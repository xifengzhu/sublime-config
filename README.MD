## Bulk install packages in Sublime Text 2

**Install Sublime Text 2**

**Install Package Control(View > Show Console)**

```
import urllib2,os,hashlib; h = '2915d1851351e5ee549c20394736b442' + '8bc59f460fa1548d1514676163dafc88'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
```

**Import sublime config from github repo**

```
cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/User/

git clone git@github.com:xifengzhu/sublime-config.git

mv sublime-config/* .

rm -rf sublime-config

```

**Restart Sublime Text and allow it to pick up and install the new packages**

