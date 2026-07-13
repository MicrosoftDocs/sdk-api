---
UID: NF:winuser.SystemParametersInfoW
title: SystemParametersInfoW function (winuser.h)
description: Retrieves or sets the value of one of the system-wide parameters. (Unicode)
prerelease: true
helpviewer_keywords: ["SPIF_SENDCHANGE", "SPIF_SENDWININICHANGE", "SPIF_UPDATEINIFILE", "SPI_GETACCESSTIMEOUT", "SPI_GETACTIVEWINDOWTRACKING", "SPI_GETACTIVEWNDTRKTIMEOUT", "SPI_GETACTIVEWNDTRKZORDER", "SPI_GETANIMATION", "SPI_GETAUDIODESCRIPTION", "SPI_GETBEEP", "SPI_GETBLOCKSENDINPUTRESETS", "SPI_GETBORDER", "SPI_GETCARETWIDTH", "SPI_GETCLEARTYPE", "SPI_GETCLIENTAREAANIMATION", "SPI_GETCOMBOBOXANIMATION", "SPI_GETCONTACTVISUALIZATION", "SPI_GETCURSORSHADOW", "SPI_GETDEFAULTINPUTLANG", "SPI_GETDESKWALLPAPER", "SPI_GETDISABLEOVERLAPPEDCONTENT", "SPI_GETDOCKMOVING", "SPI_GETDRAGFROMMAXIMIZE", "SPI_GETDRAGFULLWINDOWS", "SPI_GETDROPSHADOW", "SPI_GETFILTERKEYS", "SPI_GETFLATMENU", "SPI_GETFOCUSBORDERHEIGHT", "SPI_GETFOCUSBORDERWIDTH", "SPI_GETFONTSMOOTHING", "SPI_GETFONTSMOOTHINGCONTRAST", "SPI_GETFONTSMOOTHINGORIENTATION", "SPI_GETFONTSMOOTHINGTYPE", "SPI_GETFOREGROUNDFLASHCOUNT", "SPI_GETFOREGROUNDLOCKTIMEOUT", "SPI_GETGESTUREVISUALIZATION", "SPI_GETGRADIENTCAPTIONS", "SPI_GETHIGHCONTRAST", "SPI_GETHOTTRACKING", "SPI_GETHUNGAPPTIMEOUT", "SPI_GETICONMETRICS", "SPI_GETICONTITLELOGFONT", "SPI_GETICONTITLEWRAP", "SPI_GETKEYBOARDCUES", "SPI_GETKEYBOARDDELAY", "SPI_GETKEYBOARDPREF", "SPI_GETKEYBOARDSPEED", "SPI_GETLISTBOXSMOOTHSCROLLING", "SPI_GETLOGICALDPIOVERRIDE", "SPI_GETLOWPOWERACTIVE", "SPI_GETLOWPOWERTIMEOUT", "SPI_GETMENUANIMATION", "SPI_GETMENUDROPALIGNMENT", "SPI_GETMENUFADE", "SPI_GETMENUSHOWDELAY", "SPI_GETMENUUNDERLINES", "SPI_GETMESSAGEDURATION", "SPI_GETMINIMIZEDMETRICS", "SPI_GETMOUSE", "SPI_GETMOUSECLICKLOCK", "SPI_GETMOUSECLICKLOCKTIME", "SPI_GETMOUSEDOCKTHRESHOLD", "SPI_GETMOUSEDRAGOUTTHRESHOLD", "SPI_GETMOUSEHOVERHEIGHT", "SPI_GETMOUSEHOVERTIME", "SPI_GETMOUSEHOVERWIDTH", "SPI_GETMOUSEKEYS", "SPI_GETMOUSESIDEMOVETHRESHOLD", "SPI_GETMOUSESONAR", "SPI_GETMOUSESPEED", "SPI_GETMOUSETRAILS", "SPI_GETMOUSEVANISH", "SPI_GETMOUSEWHEELROUTING", "SPI_GETNONCLIENTMETRICS", "SPI_GETPENDOCKTHRESHOLD", "SPI_GETPENDRAGOUTTHRESHOLD", "SPI_GETPENSIDEMOVETHRESHOLD", "SPI_GETPENVISUALIZATION", "SPI_GETPOWEROFFACTIVE", "SPI_GETPOWEROFFTIMEOUT", "SPI_GETSCREENREADER", "SPI_GETSCREENSAVEACTIVE", "SPI_GETSCREENSAVERRUNNING", "SPI_GETSCREENSAVESECURE", "SPI_GETSCREENSAVETIMEOUT", "SPI_GETSELECTIONFADE", "SPI_GETSERIALKEYS", "SPI_GETSHOWIMEUI", "SPI_GETSHOWSOUNDS", "SPI_GETSNAPSIZING", "SPI_GETSNAPTODEFBUTTON", "SPI_GETSOUNDSENTRY", "SPI_GETSTICKYKEYS", "SPI_GETSYSTEMLANGUAGEBAR", "SPI_GETTHREADLOCALINPUTSETTINGS", "SPI_GETTOGGLEKEYS", "SPI_GETTOOLTIPANIMATION", "SPI_GETTOOLTIPFADE", "SPI_GETUIEFFECTS", "SPI_GETWAITTOKILLSERVICETIMEOUT", "SPI_GETWAITTOKILLTIMEOUT", "SPI_GETWHEELSCROLLCHARS", "SPI_GETWHEELSCROLLLINES", "SPI_GETWINARRANGING", "SPI_GETWORKAREA", "SPI_ICONHORIZONTALSPACING", "SPI_ICONVERTICALSPACING", "SPI_SETACCESSTIMEOUT", "SPI_SETACTIVEWINDOWTRACKING", "SPI_SETACTIVEWNDTRKTIMEOUT", "SPI_SETACTIVEWNDTRKZORDER", "SPI_SETANIMATION", "SPI_SETAUDIODESCRIPTION", "SPI_SETBEEP", "SPI_SETBLOCKSENDINPUTRESETS", "SPI_SETBORDER", "SPI_SETCARETWIDTH", "SPI_SETCLEARTYPE", "SPI_SETCLIENTAREAANIMATION", "SPI_SETCOMBOBOXANIMATION", "SPI_SETCONTACTVISUALIZATION", "SPI_SETCURSORS", "SPI_SETCURSORSHADOW", "SPI_SETDEFAULTINPUTLANG", "SPI_SETDESKPATTERN", "SPI_SETDESKWALLPAPER", "SPI_SETDISABLEOVERLAPPEDCONTENT", "SPI_SETDOCKMOVING", "SPI_SETDOUBLECLICKTIME", "SPI_SETDOUBLECLKHEIGHT", "SPI_SETDOUBLECLKWIDTH", "SPI_SETDRAGFROMMAXIMIZE", "SPI_SETDRAGFULLWINDOWS", "SPI_SETDRAGHEIGHT", "SPI_SETDRAGWIDTH", "SPI_SETDROPSHADOW", "SPI_SETFILTERKEYS", "SPI_SETFLATMENU", "SPI_SETFOCUSBORDERHEIGHT", "SPI_SETFOCUSBORDERWIDTH", "SPI_SETFONTSMOOTHING", "SPI_SETFONTSMOOTHINGCONTRAST", "SPI_SETFONTSMOOTHINGORIENTATION", "SPI_SETFONTSMOOTHINGTYPE", "SPI_SETFOREGROUNDFLASHCOUNT", "SPI_SETFOREGROUNDLOCKTIMEOUT", "SPI_SETGESTUREVISUALIZATION", "SPI_SETGRADIENTCAPTIONS", "SPI_SETHIGHCONTRAST", "SPI_SETHOTTRACKING", "SPI_SETHUNGAPPTIMEOUT", "SPI_SETICONMETRICS", "SPI_SETICONS", "SPI_SETICONTITLELOGFONT", "SPI_SETICONTITLEWRAP", "SPI_SETKEYBOARDCUES", "SPI_SETKEYBOARDDELAY", "SPI_SETKEYBOARDPREF", "SPI_SETKEYBOARDSPEED", "SPI_SETLANGTOGGLE", "SPI_SETLISTBOXSMOOTHSCROLLING", "SPI_SETLOGICALDPIOVERRIDE", "SPI_SETLOWPOWERACTIVE", "SPI_SETLOWPOWERTIMEOUT", "SPI_SETMENUANIMATION", "SPI_SETMENUDROPALIGNMENT", "SPI_SETMENUFADE", "SPI_SETMENUSHOWDELAY", "SPI_SETMENUUNDERLINES", "SPI_SETMESSAGEDURATION", "SPI_SETMINIMIZEDMETRICS", "SPI_SETMOUSE", "SPI_SETMOUSEBUTTONSWAP", "SPI_SETMOUSECLICKLOCK", "SPI_SETMOUSECLICKLOCKTIME", "SPI_SETMOUSEDOCKTHRESHOLD", "SPI_SETMOUSEDRAGOUTTHRESHOLD", "SPI_SETMOUSEHOVERHEIGHT", "SPI_SETMOUSEHOVERTIME", "SPI_SETMOUSEHOVERWIDTH", "SPI_SETMOUSEKEYS", "SPI_SETMOUSESIDEMOVETHRESHOLD", "SPI_SETMOUSESONAR", "SPI_SETMOUSESPEED", "SPI_SETMOUSETRAILS", "SPI_SETMOUSEVANISH", "SPI_SETMOUSEWHEELROUTING", "SPI_SETNONCLIENTMETRICS", "SPI_SETPENDOCKTHRESHOLD", "SPI_SETPENDRAGOUTTHRESHOLD", "SPI_SETPENSIDEMOVETHRESHOLD", "SPI_SETPENVISUALIZATION", "SPI_SETPOWEROFFACTIVE", "SPI_SETPOWEROFFTIMEOUT", "SPI_SETSCREENREADER", "SPI_SETSCREENSAVEACTIVE", "SPI_SETSCREENSAVESECURE", "SPI_SETSCREENSAVETIMEOUT", "SPI_SETSELECTIONFADE", "SPI_SETSERIALKEYS", "SPI_SETSHOWIMEUI", "SPI_SETSHOWSOUNDS", "SPI_SETSNAPSIZING", "SPI_SETSNAPTODEFBUTTON", "SPI_SETSOUNDSENTRY", "SPI_SETSTICKYKEYS", "SPI_SETSYSTEMLANGUAGEBAR", "SPI_SETTHREADLOCALINPUTSETTINGS", "SPI_SETTOGGLEKEYS", "SPI_SETTOOLTIPANIMATION", "SPI_SETTOOLTIPFADE", "SPI_SETUIEFFECTS", "SPI_SETWAITTOKILLSERVICETIMEOUT", "SPI_SETWAITTOKILLTIMEOUT", "SPI_SETWHEELSCROLLCHARS", "SPI_SETWHEELSCROLLLINES", "SPI_SETWINARRANGING", "SPI_SETWORKAREA", "SystemParametersInfo", "SystemParametersInfo function [Windows and Messages]", "SystemParametersInfoW", "_win32_systemparametersinfo", "base.systemparametersinfo", "systemparametersinfo_cpp", "winmsg.systemparametersinfo", "winui.systemparametersinfo", "winuser/SystemParametersInfo", "winuser/SystemParametersInfoW"]
old-location: winmsg\systemparametersinfo.htm
tech.root: winmsg
ms.assetid: 9b99465c-e12d-413c-8e69-b46b52f2f11f
ms.date: 03/27/2024
ms.keywords: SPIF_SENDCHANGE, SPIF_SENDWININICHANGE, SPIF_UPDATEINIFILE, SPI_GETACCESSTIMEOUT, SPI_GETACTIVEWINDOWTRACKING, SPI_GETACTIVEWNDTRKTIMEOUT, SPI_GETACTIVEWNDTRKZORDER, SPI_GETANIMATION, SPI_GETAUDIODESCRIPTION, SPI_GETBEEP, SPI_GETBLOCKSENDINPUTRESETS, SPI_GETBORDER, SPI_GETCARETWIDTH, SPI_GETCLEARTYPE, SPI_GETCLIENTAREAANIMATION, SPI_GETCOMBOBOXANIMATION, SPI_GETCONTACTVISUALIZATION, SPI_GETCURSORSHADOW, SPI_GETDEFAULTINPUTLANG, SPI_GETDESKWALLPAPER, SPI_GETDISABLEOVERLAPPEDCONTENT, SPI_GETDOCKMOVING, SPI_GETDRAGFROMMAXIMIZE, SPI_GETDRAGFULLWINDOWS, SPI_GETDROPSHADOW, SPI_GETFILTERKEYS, SPI_GETFLATMENU, SPI_GETFOCUSBORDERHEIGHT, SPI_GETFOCUSBORDERWIDTH, SPI_GETFONTSMOOTHING, SPI_GETFONTSMOOTHINGCONTRAST, SPI_GETFONTSMOOTHINGORIENTATION, SPI_GETFONTSMOOTHINGTYPE, SPI_GETFOREGROUNDFLASHCOUNT, SPI_GETFOREGROUNDLOCKTIMEOUT, SPI_GETGESTUREVISUALIZATION, SPI_GETGRADIENTCAPTIONS, SPI_GETHIGHCONTRAST, SPI_GETHOTTRACKING, SPI_GETHUNGAPPTIMEOUT, SPI_GETICONMETRICS, SPI_GETICONTITLELOGFONT, SPI_GETICONTITLEWRAP, SPI_GETKEYBOARDCUES, SPI_GETKEYBOARDDELAY, SPI_GETKEYBOARDPREF, SPI_GETKEYBOARDSPEED, SPI_GETLISTBOXSMOOTHSCROLLING, SPI_GETLOGICALDPIOVERRIDE, SPI_GETLOWPOWERACTIVE, SPI_GETLOWPOWERTIMEOUT, SPI_GETMENUANIMATION, SPI_GETMENUDROPALIGNMENT, SPI_GETMENUFADE, SPI_GETMENUSHOWDELAY, SPI_GETMENUUNDERLINES, SPI_GETMESSAGEDURATION, SPI_GETMINIMIZEDMETRICS, SPI_GETMOUSE, SPI_GETMOUSECLICKLOCK, SPI_GETMOUSECLICKLOCKTIME, SPI_GETMOUSEDOCKTHRESHOLD, SPI_GETMOUSEDRAGOUTTHRESHOLD, SPI_GETMOUSEHOVERHEIGHT, SPI_GETMOUSEHOVERTIME, SPI_GETMOUSEHOVERWIDTH, SPI_GETMOUSEKEYS, SPI_GETMOUSESIDEMOVETHRESHOLD, SPI_GETMOUSESONAR, SPI_GETMOUSESPEED, SPI_GETMOUSETRAILS, SPI_GETMOUSEVANISH, SPI_GETMOUSEWHEELROUTING, SPI_GETNONCLIENTMETRICS, SPI_GETPENDOCKTHRESHOLD, SPI_GETPENDRAGOUTTHRESHOLD, SPI_GETPENSIDEMOVETHRESHOLD, SPI_GETPENVISUALIZATION, SPI_GETPOWEROFFACTIVE, SPI_GETPOWEROFFTIMEOUT, SPI_GETSCREENREADER, SPI_GETSCREENSAVEACTIVE, SPI_GETSCREENSAVERRUNNING, SPI_GETSCREENSAVESECURE, SPI_GETSCREENSAVETIMEOUT, SPI_GETSELECTIONFADE, SPI_GETSERIALKEYS, SPI_GETSHOWIMEUI, SPI_GETSHOWSOUNDS, SPI_GETSNAPSIZING, SPI_GETSNAPTODEFBUTTON, SPI_GETSOUNDSENTRY, SPI_GETSTICKYKEYS, SPI_GETSYSTEMLANGUAGEBAR, SPI_GETTHREADLOCALINPUTSETTINGS, SPI_GETTOGGLEKEYS, SPI_GETTOOLTIPANIMATION, SPI_GETTOOLTIPFADE, SPI_GETUIEFFECTS, SPI_GETWAITTOKILLSERVICETIMEOUT, SPI_GETWAITTOKILLTIMEOUT, SPI_GETWHEELSCROLLCHARS, SPI_GETWHEELSCROLLLINES, SPI_GETWINARRANGING, SPI_GETWORKAREA, SPI_ICONHORIZONTALSPACING, SPI_ICONVERTICALSPACING, SPI_SETACCESSTIMEOUT, SPI_SETACTIVEWINDOWTRACKING, SPI_SETACTIVEWNDTRKTIMEOUT, SPI_SETACTIVEWNDTRKZORDER, SPI_SETANIMATION, SPI_SETAUDIODESCRIPTION, SPI_SETBEEP, SPI_SETBLOCKSENDINPUTRESETS, SPI_SETBORDER, SPI_SETCARETWIDTH, SPI_SETCLEARTYPE, SPI_SETCLIENTAREAANIMATION, SPI_SETCOMBOBOXANIMATION, SPI_SETCONTACTVISUALIZATION, SPI_SETCURSORS, SPI_SETCURSORSHADOW, SPI_SETDEFAULTINPUTLANG, SPI_SETDESKPATTERN, SPI_SETDESKWALLPAPER, SPI_SETDISABLEOVERLAPPEDCONTENT, SPI_SETDOCKMOVING, SPI_SETDOUBLECLICKTIME, SPI_SETDOUBLECLKHEIGHT, SPI_SETDOUBLECLKWIDTH, SPI_SETDRAGFROMMAXIMIZE, SPI_SETDRAGFULLWINDOWS, SPI_SETDRAGHEIGHT, SPI_SETDRAGWIDTH, SPI_SETDROPSHADOW, SPI_SETFILTERKEYS, SPI_SETFLATMENU, SPI_SETFOCUSBORDERHEIGHT, SPI_SETFOCUSBORDERWIDTH, SPI_SETFONTSMOOTHING, SPI_SETFONTSMOOTHINGCONTRAST, SPI_SETFONTSMOOTHINGORIENTATION, SPI_SETFONTSMOOTHINGTYPE, SPI_SETFOREGROUNDFLASHCOUNT, SPI_SETFOREGROUNDLOCKTIMEOUT, SPI_SETGESTUREVISUALIZATION, SPI_SETGRADIENTCAPTIONS, SPI_SETHIGHCONTRAST, SPI_SETHOTTRACKING, SPI_SETHUNGAPPTIMEOUT, SPI_SETICONMETRICS, SPI_SETICONS, SPI_SETICONTITLELOGFONT, SPI_SETICONTITLEWRAP, SPI_SETKEYBOARDCUES, SPI_SETKEYBOARDDELAY, SPI_SETKEYBOARDPREF, SPI_SETKEYBOARDSPEED, SPI_SETLANGTOGGLE, SPI_SETLISTBOXSMOOTHSCROLLING, SPI_SETLOGICALDPIOVERRIDE, SPI_SETLOWPOWERACTIVE, SPI_SETLOWPOWERTIMEOUT, SPI_SETMENUANIMATION, SPI_SETMENUDROPALIGNMENT, SPI_SETMENUFADE, SPI_SETMENUSHOWDELAY, SPI_SETMENUUNDERLINES, SPI_SETMESSAGEDURATION, SPI_SETMINIMIZEDMETRICS, SPI_SETMOUSE, SPI_SETMOUSEBUTTONSWAP, SPI_SETMOUSECLICKLOCK, SPI_SETMOUSECLICKLOCKTIME, SPI_SETMOUSEDOCKTHRESHOLD, SPI_SETMOUSEDRAGOUTTHRESHOLD, SPI_SETMOUSEHOVERHEIGHT, SPI_SETMOUSEHOVERTIME, SPI_SETMOUSEHOVERWIDTH, SPI_SETMOUSEKEYS, SPI_SETMOUSESIDEMOVETHRESHOLD, SPI_SETMOUSESONAR, SPI_SETMOUSESPEED, SPI_SETMOUSETRAILS, SPI_SETMOUSEVANISH, SPI_SETMOUSEWHEELROUTING, SPI_SETNONCLIENTMETRICS, SPI_SETPENDOCKTHRESHOLD, SPI_SETPENDRAGOUTTHRESHOLD, SPI_SETPENSIDEMOVETHRESHOLD, SPI_SETPENVISUALIZATION, SPI_SETPOWEROFFACTIVE, SPI_SETPOWEROFFTIMEOUT, SPI_SETSCREENREADER, SPI_SETSCREENSAVEACTIVE, SPI_SETSCREENSAVESECURE, SPI_SETSCREENSAVETIMEOUT, SPI_SETSELECTIONFADE, SPI_SETSERIALKEYS, SPI_SETSHOWIMEUI, SPI_SETSHOWSOUNDS, SPI_SETSNAPSIZING, SPI_SETSNAPTODEFBUTTON, SPI_SETSOUNDSENTRY, SPI_SETSTICKYKEYS, SPI_SETSYSTEMLANGUAGEBAR, SPI_SETTHREADLOCALINPUTSETTINGS, SPI_SETTOGGLEKEYS, SPI_SETTOOLTIPANIMATION, SPI_SETTOOLTIPFADE, SPI_SETUIEFFECTS, SPI_SETWAITTOKILLSERVICETIMEOUT, SPI_SETWAITTOKILLTIMEOUT, SPI_SETWHEELSCROLLCHARS, SPI_SETWHEELSCROLLLINES, SPI_SETWINARRANGING, SPI_SETWORKAREA, SystemParametersInfo, SystemParametersInfo function [Windows and Messages], SystemParametersInfoA, SystemParametersInfoW, _win32_systemparametersinfo, base.systemparametersinfo, systemparametersinfo_cpp, winmsg.systemparametersinfo, winui.systemparametersinfo, winuser/SystemParametersInfo, winuser/SystemParametersInfoA, winuser/SystemParametersInfoW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SystemParametersInfoW (Unicode) and SystemParametersInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SystemParametersInfoW
 - winuser/SystemParametersInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-sysparams-ext-l1-1-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-sysparams-Ext-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-sysparams-l1-1-0.dll
api_name:
 - SystemParametersInfo
 - SystemParametersInfoA
 - SystemParametersInfoW
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-0 (introduced in Windows 8)
---

# SystemParametersInfoW function


## -description

Retrieves or sets the value of one of the system-wide parameters. This function can also update the user profile while setting a parameter.

## -parameters

### -param uiAction [in]

Type: <b>UINT</b>

The system-wide parameter to be retrieved or set. The possible values are organized in the following tables of related parameters:                            

<ul>
<li>Accessibility parameters</li>
<li>Desktop parameters</li>
<li>Icon parameters</li>
<li>Input parameters</li>
<li>Menu parameters</li>
<li>Power parameters</li>
<li>Screen saver parameters</li>
<li>Time-out parameters</li>
<li>UI effect parameters</li>
<li>Window parameters</li>
</ul>


The following are the accessibility parameters.

<table>
<tr>
<th>Accessibility parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETACCESSTIMEOUT"></a><a id="spi_getaccesstimeout"></a><dl>
<dt><b>SPI_GETACCESSTIMEOUT</b></dt>
<dt>0x003C</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the time-out period associated with the accessibility features. The <i>pvParam</i> parameter must point to an <a href="/windows/desktop/api/winuser/ns-winuser-accesstimeout">ACCESSTIMEOUT</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(ACCESSTIMEOUT)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETAUDIODESCRIPTION"></a><a id="spi_getaudiodescription"></a><dl>
<dt><b>SPI_GETAUDIODESCRIPTION</b></dt>
<dt>0x0074</dt>
</dl>
</td>
<td width="60%">
Determines whether audio descriptions are enabled or disabled. The <i>pvParam</i> parameter is a pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-audiodescription">AUDIODESCRIPTION</a> structure. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(AUDIODESCRIPTION)</code>.

While it is possible for users who have visual impairments to hear the audio in video content, there is a lot of action in video that does not have corresponding audio. Specific audio description of what is happening in a video helps these users understand the content better. This flag enables you to determine whether audio descriptions have been enabled and in which language.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETCLIENTAREAANIMATION"></a><a id="spi_getclientareaanimation"></a><dl>
<dt><b>SPI_GETCLIENTAREAANIMATION</b></dt>
<dt>0x1042</dt>
</dl>
</td>
<td width="60%">
Determines whether animations are enabled or disabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if animations are enabled, or <b>FALSE</b> otherwise.

Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy. This flag enables you to determine whether such animations have been disabled in the client area.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETDISABLEOVERLAPPEDCONTENT"></a><a id="spi_getdisableoverlappedcontent"></a><dl>
<dt><b>SPI_GETDISABLEOVERLAPPEDCONTENT</b></dt>
<dt>0x1040</dt>
</dl>
</td>
<td width="60%">
Determines whether overlapped content is enabled or disabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> otherwise.

Display features such as background images, textured backgrounds, water marks on documents, alpha blending, and transparency can reduce the contrast between the foreground and background, making it harder for users with low vision to see objects on the screen. This flag enables you to determine whether such overlapped content has been disabled.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFILTERKEYS"></a><a id="spi_getfilterkeys"></a><dl>
<dt><b>SPI_GETFILTERKEYS</b></dt>
<dt>0x0032</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the FilterKeys accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-filterkeys">FILTERKEYS</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(FILTERKEYS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFOCUSBORDERHEIGHT"></a><a id="spi_getfocusborderheight"></a><dl>
<dt><b>SPI_GETFOCUSBORDERHEIGHT</b></dt>
<dt>0x2010</dt>
</dl>
</td>
<td width="60%">
Retrieves the height, in pixels, of the top and bottom edges of the focus rectangle drawn with <a href="/windows/desktop/api/winuser/nf-winuser-drawfocusrect">DrawFocusRect</a>. The <i>pvParam</i> parameter must point to a <b>UINT</b> value.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFOCUSBORDERWIDTH"></a><a id="spi_getfocusborderwidth"></a><dl>
<dt><b>SPI_GETFOCUSBORDERWIDTH</b></dt>
<dt>0x200E</dt>
</dl>
</td>
<td width="60%">
Retrieves the width, in pixels, of the left and right edges of the focus rectangle drawn with <a href="/windows/desktop/api/winuser/nf-winuser-drawfocusrect">DrawFocusRect</a>. The <i>pvParam</i> parameter must point to a <b>UINT</b>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETHIGHCONTRAST"></a><a id="spi_gethighcontrast"></a><dl>
<dt><b>SPI_GETHIGHCONTRAST</b></dt>
<dt>0x0042</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the HighContrast accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-highcontrasta">HIGHCONTRAST</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(HIGHCONTRAST)</code>.

For a general discussion, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETLOGICALDPIOVERRIDE"></a><a id="spi_getlogicaldpioverride"></a><dl>
<dt><b>SPI_GETLOGICALDPIOVERRIDE</b></dt>
<dt>0x009E</dt>
</dl>
</td>
<td width="60%">
Retrieves a value that determines whether Windows 8 is displaying apps using the default scaling plateau for the hardware or going to the next higher plateau. This value is based on the current "Make everything on your screen bigger" setting, found in the <b>Ease of Access</b> section of <b>PC settings</b>: 1 is on, 0 is off.

Apps can provide text and image resources for each of several scaling plateaus: 100%, 140%, and 180%. Providing separate resources optimized for a particular scale avoids distortion due to resizing. Windows 8 determines the appropriate scaling plateau based on a number of factors, including screen size and pixel density. When "Make everything on your screen bigger" is selected (SPI_GETLOGICALDPIOVERRIDE returns a value of 1), Windows uses resources from the next higher plateau. For example, in the case of hardware that Windows determines should use a scale of <a href="/windows/desktop/api/shtypes/ne-shtypes-device_scale_factor">SCALE_100_PERCENT</a>, this override causes Windows to use the <a href="/windows/desktop/api/shtypes/ne-shtypes-device_scale_factor">SCALE_140_PERCENT</a> scale value, assuming that it does not violate other constraints.

<div class="alert"><b>Note</b>  You should not use this value. It might be altered or unavailable in subsequent versions of Windows. Instead, use the <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorfordevice">GetScaleFactorForDevice</a> function or the <a href="/uwp/api/Windows.Graphics.Display.DisplayProperties">DisplayProperties</a> class to retrieve the preferred scaling factor. Desktop applications should use desktop logical DPI rather than scale factor. Desktop logical DPI can be retrieved through the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMESSAGEDURATION"></a><a id="spi_getmessageduration"></a><dl>
<dt><b>SPI_GETMESSAGEDURATION</b></dt>
<dt>0x2016</dt>
</dl>
</td>
<td width="60%">
Retrieves the time that notification pop-ups should be displayed, in seconds. The <i>pvParam</i> parameter must point to a <b>ULONG</b> that receives the message duration.

Users with visual impairments or cognitive conditions such as ADHD and dyslexia might need a longer time to read the text in notification messages. This flag enables you to retrieve the message duration.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSECLICKLOCK"></a><a id="spi_getmouseclicklock"></a><dl>
<dt><b>SPI_GETMOUSECLICKLOCK</b></dt>
<dt>0x101E</dt>
</dl>
</td>
<td width="60%">
Retrieves the state of the Mouse ClickLock feature. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> otherwise. For more information, see <a href="/windows/desktop/inputdev/about-mouse-input">Mouse Input Overview</a>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSECLICKLOCKTIME"></a><a id="spi_getmouseclicklocktime"></a><dl>
<dt><b>SPI_GETMOUSECLICKLOCKTIME</b></dt>
<dt>0x2008</dt>
</dl>
</td>
<td width="60%">
Retrieves the time delay before the primary mouse button is locked. The <i>pvParam</i> parameter must point to <b>DWORD</b> that receives the time delay, in milliseconds. This is only enabled if <b>SPI_SETMOUSECLICKLOCK</b> is set to <b>TRUE</b>. For more information, see <a href="/windows/desktop/inputdev/about-mouse-input">Mouse Input Overview</a>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSEKEYS"></a><a id="spi_getmousekeys"></a><dl>
<dt><b>SPI_GETMOUSEKEYS</b></dt>
<dt>0x0036</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the MouseKeys accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-mousekeys">MOUSEKEYS</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(MOUSEKEYS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSESONAR"></a><a id="spi_getmousesonar"></a><dl>
<dt><b>SPI_GETMOUSESONAR</b></dt>
<dt>0x101C</dt>
</dl>
</td>
<td width="60%">
Retrieves the state of the Mouse Sonar feature. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled or <b>FALSE</b> otherwise. For more information, see <a href="/windows/desktop/inputdev/about-mouse-input">Mouse Input Overview</a>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSEVANISH"></a><a id="spi_getmousevanish"></a><dl>
<dt><b>SPI_GETMOUSEVANISH</b></dt>
<dt>0x1020</dt>
</dl>
</td>
<td width="60%">
Retrieves the state of the Mouse Vanish feature. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled or <b>FALSE</b> otherwise. For more information, see <a href="/windows/desktop/inputdev/about-mouse-input">Mouse Input Overview</a>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSCREENREADER"></a><a id="spi_getscreenreader"></a><dl>
<dt><b>SPI_GETSCREENREADER</b></dt>
<dt>0x0046</dt>
</dl>
</td>
<td width="60%">
Determines whether a screen reviewer utility is running. A screen reviewer utility directs textual information to an output device, such as a speech synthesizer or Braille display. When this flag is set, an application should provide textual information in situations where it would otherwise present the information  graphically.

The <i>pvParam</i> parameter is a pointer to a <b>BOOL</b> variable that receives <b>TRUE</b> if a screen reviewer utility is running, or <b>FALSE</b> otherwise.

<div class="alert"><b>Note</b>  Narrator, the screen reader that is included with Windows, does not set the <b>SPI_SETSCREENREADER</b> or <b>SPI_GETSCREENREADER</b> flags.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSERIALKEYS"></a><a id="spi_getserialkeys"></a><dl>
<dt><b>SPI_GETSERIALKEYS</b></dt>
<dt>0x003E</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported.

<b>Windows Server 2003 and Windows XP/2000:  </b>The user should control this setting through the Control Panel.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSHOWSOUNDS"></a><a id="spi_getshowsounds"></a><dl>
<dt><b>SPI_GETSHOWSOUNDS</b></dt>
<dt>0x0038</dt>
</dl>
</td>
<td width="60%">
Determines whether the Show Sounds accessibility flag is on or off. If it is on, the user requires an application to present information visually in situations where it would otherwise present the information only in audible form. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the feature is on, or <b>FALSE</b> if it is off.

Using this value is equivalent to calling <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with <b>SM_SHOWSOUNDS</b>. That is the recommended call.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSOUNDSENTRY"></a><a id="spi_getsoundsentry"></a><dl>
<dt><b>SPI_GETSOUNDSENTRY</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the SoundSentry accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-soundsentrya">SOUNDSENTRY</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(SOUNDSENTRY)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSTICKYKEYS"></a><a id="spi_getstickykeys"></a><dl>
<dt><b>SPI_GETSTICKYKEYS</b></dt>
<dt>0x003A</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the StickyKeys accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-stickykeys">STICKYKEYS</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(STICKYKEYS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETTOGGLEKEYS"></a><a id="spi_gettogglekeys"></a><dl>
<dt><b>SPI_GETTOGGLEKEYS</b></dt>
<dt>0x0034</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the ToggleKeys accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-togglekeys">TOGGLEKEYS</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(TOGGLEKEYS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETACCESSTIMEOUT"></a><a id="spi_setaccesstimeout"></a><dl>
<dt><b>SPI_SETACCESSTIMEOUT</b></dt>
<dt>0x003D</dt>
</dl>
</td>
<td width="60%">
Sets the time-out period associated with the accessibility features. The <i>pvParam</i> parameter must point to an <a href="/windows/desktop/api/winuser/ns-winuser-accesstimeout">ACCESSTIMEOUT</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(ACCESSTIMEOUT)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETAUDIODESCRIPTION"></a><a id="spi_setaudiodescription"></a><dl>
<dt><b>SPI_SETAUDIODESCRIPTION</b></dt>
<dt>0x0075</dt>
</dl>
</td>
<td width="60%">
Turns the audio descriptions feature on or off. The <i>pvParam</i> parameter is a pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-audiodescription">AUDIODESCRIPTION</a> structure.

While it is possible for users who are visually impaired to hear the audio in video content, there is a lot of action in video that does not have corresponding audio. Specific audio description of what is happening in a video helps these users understand the content better. This flag enables you to enable or disable audio descriptions in the languages they are provided in.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETCLIENTAREAANIMATION"></a><a id="spi_setclientareaanimation"></a><dl>
<dt><b>SPI_SETCLIENTAREAANIMATION</b></dt>
<dt>0x1043</dt>
</dl>
</td>
<td width="60%">
Turns client area animations on or off. The <i>pvParam</i> parameter is a <b>BOOL</b> variable. Set <i>pvParam</i> to <b>TRUE</b> to enable animations and other transient effects in the client area, or <b>FALSE</b> to disable them.

Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy. This flag enables you to enable or disable all such animations.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDISABLEOVERLAPPEDCONTENT"></a><a id="spi_setdisableoverlappedcontent"></a><dl>
<dt><b>SPI_SETDISABLEOVERLAPPEDCONTENT</b></dt>
<dt>0x1041</dt>
</dl>
</td>
<td width="60%">
Turns overlapped content (such as background images and watermarks) on or off. The <i>pvParam</i> parameter is a <b>BOOL</b> variable. Set <i>pvParam</i> to <b>TRUE</b> to disable overlapped content, or <b>FALSE</b> to enable overlapped content.

Display features such as background images, textured backgrounds, water marks on documents, alpha blending, and transparency can reduce the contrast between the foreground and background, making it harder for users with low vision to see objects on the screen. This flag enables you to enable or disable all such overlapped content.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFILTERKEYS"></a><a id="spi_setfilterkeys"></a><dl>
<dt><b>SPI_SETFILTERKEYS</b></dt>
<dt>0x0033</dt>
</dl>
</td>
<td width="60%">
Sets the parameters of the FilterKeys accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-filterkeys">FILTERKEYS</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(FILTERKEYS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFOCUSBORDERHEIGHT"></a><a id="spi_setfocusborderheight"></a><dl>
<dt><b>SPI_SETFOCUSBORDERHEIGHT</b></dt>
<dt>0x2011</dt>
</dl>
</td>
<td width="60%">
Sets the height of the top and bottom edges of the focus rectangle drawn with <a href="/windows/desktop/api/winuser/nf-winuser-drawfocusrect">DrawFocusRect</a> to the value of the <i>pvParam</i> parameter.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFOCUSBORDERWIDTH"></a><a id="spi_setfocusborderwidth"></a><dl>
<dt><b>SPI_SETFOCUSBORDERWIDTH</b></dt>
<dt>0x200F</dt>
</dl>
</td>
<td width="60%">
Sets the height of the left and right edges of the focus rectangle drawn with <a href="/windows/desktop/api/winuser/nf-winuser-drawfocusrect">DrawFocusRect</a> to the value of the <i>pvParam</i> parameter.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETHIGHCONTRAST"></a><a id="spi_sethighcontrast"></a><dl>
<dt><b>SPI_SETHIGHCONTRAST</b></dt>
<dt>0x0043</dt>
</dl>
</td>
<td width="60%">
Sets the parameters of the HighContrast accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-highcontrasta">HIGHCONTRAST</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(HIGHCONTRAST)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETLOGICALDPIOVERRIDE"></a><a id="spi_setlogicaldpioverride"></a><dl>
<dt><b>SPI_SETLOGICALDPIOVERRIDE</b></dt>
<dt>0x009F</dt>
</dl>
</td>
<td width="60%">
Do not use.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMESSAGEDURATION"></a><a id="spi_setmessageduration"></a><dl>
<dt><b>SPI_SETMESSAGEDURATION</b></dt>
<dt>0x2017</dt>
</dl>
</td>
<td width="60%">
Sets the time that notification pop-ups should be displayed, in seconds. The <i>pvParam</i> parameter specifies the message duration.

Users with visual impairments or cognitive conditions such as ADHD and dyslexia might need a longer time to read the text in notification messages. This flag enables you to set the message duration.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSECLICKLOCK"></a><a id="spi_setmouseclicklock"></a><dl>
<dt><b>SPI_SETMOUSECLICKLOCK</b></dt>
<dt>0x101F</dt>
</dl>
</td>
<td width="60%">
Turns the Mouse ClickLock accessibility feature on or off. This feature temporarily locks down the primary mouse button when that button is clicked and held down for the time specified by <b>SPI_SETMOUSECLICKLOCKTIME</b>. The <i>pvParam</i> parameter specifies <b>TRUE</b> for on, or <b>FALSE</b> for off. The default is off. For more information, see Remarks and <a href="/windows/desktop/inputdev/about-mouse-input">AboutMouse Input</a>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSECLICKLOCKTIME"></a><a id="spi_setmouseclicklocktime"></a><dl>
<dt><b>SPI_SETMOUSECLICKLOCKTIME</b></dt>
<dt>0x2009</dt>
</dl>
</td>
<td width="60%">
Adjusts the time delay before the primary mouse button is locked. The <i>uiParam</i> parameter should be set to 0. The <i>pvParam</i> parameter points to a <b>DWORD</b> that specifies the time delay in milliseconds. For example, specify 1000 for a 1 second delay. The default is 1200. For more information, see <a href="/windows/desktop/inputdev/about-mouse-input">Mouse Input Overview</a>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEKEYS"></a><a id="spi_setmousekeys"></a><dl>
<dt><b>SPI_SETMOUSEKEYS</b></dt>
<dt>0x0037</dt>
</dl>
</td>
<td width="60%">
Sets the parameters of the MouseKeys accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-mousekeys">MOUSEKEYS</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(MOUSEKEYS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSESONAR"></a><a id="spi_setmousesonar"></a><dl>
<dt><b>SPI_SETMOUSESONAR</b></dt>
<dt>0x101D</dt>
</dl>
</td>
<td width="60%">
Turns the Sonar accessibility feature on or off. This feature briefly shows several concentric circles around the mouse pointer when the user presses and releases the CTRL key. The <i>pvParam</i> parameter specifies <b>TRUE</b> for on and <b>FALSE</b> for off. The default is off. For more information, see <a href="/windows/desktop/inputdev/about-mouse-input">Mouse Input Overview</a>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEVANISH"></a><a id="spi_setmousevanish"></a><dl>
<dt><b>SPI_SETMOUSEVANISH</b></dt>
<dt>0x1021</dt>
</dl>
</td>
<td width="60%">
Turns the Vanish feature on or off. This feature hides the mouse pointer when the user types; the pointer reappears when the user moves the mouse. The <i>pvParam</i> parameter specifies <b>TRUE</b> for on and <b>FALSE</b> for off. The default is off. For more information, see <a href="/windows/desktop/inputdev/about-mouse-input">Mouse Input Overview</a>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSCREENREADER"></a><a id="spi_setscreenreader"></a><dl>
<dt><b>SPI_SETSCREENREADER</b></dt>
<dt>0x0047</dt>
</dl>
</td>
<td width="60%">
Determines whether a screen review utility is running. The <i>uiParam</i> parameter specifies <b>TRUE</b> for on, or <b>FALSE</b> for off.

<div class="alert"><b>Note</b>  Narrator, the screen reader that is included with Windows, does not set the <b>SPI_SETSCREENREADER</b> or <b>SPI_GETSCREENREADER</b> flags.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSERIALKEYS"></a><a id="spi_setserialkeys"></a><dl>
<dt><b>SPI_SETSERIALKEYS</b></dt>
<dt>0x003F</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported.

<b>Windows Server 2003 and Windows XP/2000:  </b>The user should control this setting through the Control Panel.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSHOWSOUNDS"></a><a id="spi_setshowsounds"></a><dl>
<dt><b>SPI_SETSHOWSOUNDS</b></dt>
<dt>0x0039</dt>
</dl>
</td>
<td width="60%">
Turns the ShowSounds accessibility feature on or off. The <i>uiParam</i> parameter specifies <b>TRUE</b> for on, or <b>FALSE</b> for off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSOUNDSENTRY"></a><a id="spi_setsoundsentry"></a><dl>
<dt><b>SPI_SETSOUNDSENTRY</b></dt>
<dt>0x0041</dt>
</dl>
</td>
<td width="60%">
Sets the parameters of the <b>SoundSentry</b> accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-soundsentrya">SOUNDSENTRY</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(SOUNDSENTRY)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSTICKYKEYS"></a><a id="spi_setstickykeys"></a><dl>
<dt><b>SPI_SETSTICKYKEYS</b></dt>
<dt>0x003B</dt>
</dl>
</td>
<td width="60%">
Sets the parameters of the StickyKeys accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-stickykeys">STICKYKEYS</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(STICKYKEYS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETTOGGLEKEYS"></a><a id="spi_settogglekeys"></a><dl>
<dt><b>SPI_SETTOGGLEKEYS</b></dt>
<dt>0x0035</dt>
</dl>
</td>
<td width="60%">
Sets the parameters of the ToggleKeys accessibility feature. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-togglekeys">TOGGLEKEYS</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(TOGGLEKEYS)</code>.

</td>
</tr>
</table>
 

The following are the desktop parameters.

<table>
<tr>
<th>Desktop parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETCLEARTYPE"></a><a id="spi_getcleartype"></a><dl>
<dt><b>SPI_GETCLEARTYPE</b></dt>
<dt>0x1048</dt>
</dl>
</td>
<td width="60%">
Determines whether ClearType is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if ClearType is enabled, or <b>FALSE</b> otherwise.

ClearType is a software technology that improves the readability of text on liquid crystal display (LCD) monitors.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETDESKWALLPAPER"></a><a id="spi_getdeskwallpaper"></a><dl>
<dt><b>SPI_GETDESKWALLPAPER</b></dt>
<dt>0x0073</dt>
</dl>
</td>
<td width="60%">
Retrieves the full path of the bitmap file for the desktop wallpaper. The <i>pvParam</i> parameter must point to a buffer to receive the null-terminated path string. Set the <i>uiParam</i> parameter to the size, in characters, of the <i>pvParam</i> buffer. The returned string will not exceed <b>MAX_PATH</b> characters. If there is no desktop wallpaper, the returned string is empty.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETDROPSHADOW"></a><a id="spi_getdropshadow"></a><dl>
<dt><b>SPI_GETDROPSHADOW</b></dt>
<dt>0x1024</dt>
</dl>
</td>
<td width="60%">
Determines whether the drop shadow effect is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that returns <b>TRUE</b> if enabled or <b>FALSE</b> if disabled.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFLATMENU"></a><a id="spi_getflatmenu"></a><dl>
<dt><b>SPI_GETFLATMENU</b></dt>
<dt>0x1022</dt>
</dl>
</td>
<td width="60%">
Determines whether native User menus have flat menu appearance. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that returns <b>TRUE</b> if the flat menu appearance is set, or <b>FALSE</b> otherwise.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFONTSMOOTHING"></a><a id="spi_getfontsmoothing"></a><dl>
<dt><b>SPI_GETFONTSMOOTHING</b></dt>
<dt>0x004A</dt>
</dl>
</td>
<td width="60%">
Determines whether the font smoothing feature is enabled. This feature uses font antialiasing to make font curves appear smoother by painting pixels at different gray levels.

The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the feature is enabled, or <b>FALSE</b> if  it is not.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFONTSMOOTHINGCONTRAST"></a><a id="spi_getfontsmoothingcontrast"></a><dl>
<dt><b>SPI_GETFONTSMOOTHINGCONTRAST</b></dt>
<dt>0x200C</dt>
</dl>
</td>
<td width="60%">
Retrieves a contrast value that is used in <a href="/typography/cleartype/">ClearType</a> smoothing. The <i>pvParam</i> parameter must point to a <b>UINT</b> that receives the information. Valid contrast values are from 1000 to 2200. The default value is 1400.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFONTSMOOTHINGORIENTATION"></a><a id="spi_getfontsmoothingorientation"></a><dl>
<dt><b>SPI_GETFONTSMOOTHINGORIENTATION</b></dt>
<dt>0x2012</dt>
</dl>
</td>
<td width="60%">
Retrieves the font smoothing orientation. The <i>pvParam</i> parameter must point to a <b>UINT</b> that receives the information. The possible values are <b>FE_FONTSMOOTHINGORIENTATIONBGR</b> (blue-green-red) and <b>FE_FONTSMOOTHINGORIENTATIONRGB</b> (red-green-blue).

<b>Windows XP/2000:  </b>This parameter is not supported until Windows XP with SP2.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFONTSMOOTHINGTYPE"></a><a id="spi_getfontsmoothingtype"></a><dl>
<dt><b>SPI_GETFONTSMOOTHINGTYPE</b></dt>
<dt>0x200A</dt>
</dl>
</td>
<td width="60%">
Retrieves the type of font smoothing. The <i>pvParam</i> parameter must point to a <b>UINT</b> that receives the information. The possible values are <b>FE_FONTSMOOTHINGSTANDARD</b> and <b>FE_FONTSMOOTHINGCLEARTYPE</b>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETWORKAREA"></a><a id="spi_getworkarea"></a><dl>
<dt><b>SPI_GETWORKAREA</b></dt>
<dt>0x0030</dt>
</dl>
</td>
<td width="60%">
Retrieves the size of the work area on the primary display monitor. The work area is the portion of the screen not obscured by the system taskbar or by application desktop toolbars. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the coordinates of the work area, expressed in physical pixel size. Any DPI virtualization mode of the caller has no effect on this output.

To get the work area of a monitor other than the primary display monitor, call the <a href="/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa">GetMonitorInfo</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETCLEARTYPE"></a><a id="spi_setcleartype"></a><dl>
<dt><b>SPI_SETCLEARTYPE</b></dt>
<dt>0x1049</dt>
</dl>
</td>
<td width="60%">
Turns ClearType on or off. The <i>pvParam</i> parameter is a <b>BOOL</b> variable. Set <i>pvParam</i> to <b>TRUE</b> to enable ClearType, or <b>FALSE</b> to disable it.

ClearType is a software technology that improves the readability of text on LCD monitors.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETCURSORS"></a><a id="spi_setcursors"></a><dl>
<dt><b>SPI_SETCURSORS</b></dt>
<dt>0x0057</dt>
</dl>
</td>
<td width="60%">
Reloads the system cursors. Set the <i>uiParam</i> parameter to zero and the <i>pvParam</i> parameter to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDESKPATTERN"></a><a id="spi_setdeskpattern"></a><dl>
<dt><b>SPI_SETDESKPATTERN</b></dt>
<dt>0x0015</dt>
</dl>
</td>
<td width="60%">
Sets the current desktop pattern by causing Windows to read the <b>Pattern=</b> setting from the WIN.INI file.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDESKWALLPAPER"></a><a id="spi_setdeskwallpaper"></a><dl>
<dt><b>SPI_SETDESKWALLPAPER</b></dt>
<dt>0x0014</dt>
</dl>
</td>
<td width="60%">

<div class="alert"><b>Note</b>  When the <b>SPI_SETDESKWALLPAPER</b> flag is used, <b>SystemParametersInfo</b> returns <b>TRUE</b> unless there is an error (like when the specified file doesn't exist).</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDROPSHADOW"></a><a id="spi_setdropshadow"></a><dl>
<dt><b>SPI_SETDROPSHADOW</b></dt>
<dt>0x1025</dt>
</dl>
</td>
<td width="60%">
Enables or disables the drop shadow effect. Set <i>pvParam</i> to <b>TRUE</b> to enable the drop shadow effect or <b>FALSE</b> to disable it. You must also have <b>CS_DROPSHADOW</b> in the window class style.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFLATMENU"></a><a id="spi_setflatmenu"></a><dl>
<dt><b>SPI_SETFLATMENU</b></dt>
<dt>0x1023</dt>
</dl>
</td>
<td width="60%">
Enables or disables flat menu appearance for native User menus. Set <i>pvParam</i> to <b>TRUE</b> to enable flat menu appearance or <b>FALSE</b> to disable it.

When enabled, the menu bar uses <b>COLOR_MENUBAR</b> for the menubar background, <b>COLOR_MENU</b> for the menu-popup background, <b>COLOR_MENUHILIGHT</b> for the fill of the current menu selection, and <b>COLOR_HILIGHT</b> for the outline of the current menu selection. If disabled, menus are drawn using the same metrics and colors as in Windows 2000.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFONTSMOOTHING"></a><a id="spi_setfontsmoothing"></a><dl>
<dt><b>SPI_SETFONTSMOOTHING</b></dt>
<dt>0x004B</dt>
</dl>
</td>
<td width="60%">
Enables or disables the font smoothing feature, which uses font antialiasing to make font curves appear smoother by painting pixels at different gray levels.

To enable the feature, set the <i>uiParam</i> parameter to <b>TRUE</b>. To disable the feature, set <i>uiParam</i> to <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFONTSMOOTHINGCONTRAST"></a><a id="spi_setfontsmoothingcontrast"></a><dl>
<dt><b>SPI_SETFONTSMOOTHINGCONTRAST</b></dt>
<dt>0x200D</dt>
</dl>
</td>
<td width="60%">
Sets the contrast value used in <a href="/typography/cleartype/">ClearType</a> smoothing. The <i>pvParam</i> parameter is the contrast value. Valid contrast values are from 1000 to 2200. The default value is 1400.

<b>SPI_SETFONTSMOOTHINGTYPE</b> must also be set to <b>FE_FONTSMOOTHINGCLEARTYPE</b>.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFONTSMOOTHINGORIENTATION"></a><a id="spi_setfontsmoothingorientation"></a><dl>
<dt><b>SPI_SETFONTSMOOTHINGORIENTATION</b></dt>
<dt>0x2013</dt>
</dl>
</td>
<td width="60%">
Sets the font smoothing orientation. The <i>pvParam</i> parameter is either <b>FE_FONTSMOOTHINGORIENTATIONBGR</b> (blue-green-red) or <b>FE_FONTSMOOTHINGORIENTATIONRGB</b> (red-green-blue).

<b>Windows XP/2000:  </b>This parameter is not supported until Windows XP with SP2.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFONTSMOOTHINGTYPE"></a><a id="spi_setfontsmoothingtype"></a><dl>
<dt><b>SPI_SETFONTSMOOTHINGTYPE</b></dt>
<dt>0x200B</dt>
</dl>
</td>
<td width="60%">
Sets the font smoothing type. The <i>pvParam</i> parameter is either <b>FE_FONTSMOOTHINGSTANDARD</b>, if standard anti-aliasing is used, or <b>FE_FONTSMOOTHINGCLEARTYPE</b>, if <a href="/typography/cleartype/">ClearType</a> is used. The default is <b>FE_FONTSMOOTHINGSTANDARD</b>.

<b>SPI_SETFONTSMOOTHING</b> must also be set.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETWORKAREA"></a><a id="spi_setworkarea"></a><dl>
<dt><b>SPI_SETWORKAREA</b></dt>
<dt>0x002F</dt>
</dl>
</td>
<td width="60%">
Sets the size of the work area. The work area is the portion of the screen not obscured by the system taskbar or by application desktop toolbars. The <i>pvParam</i> parameter is a pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the new work area rectangle, expressed in virtual screen coordinates. In a system with multiple display monitors, the function sets the work area of the monitor that contains the specified rectangle.

</td>
</tr>
</table>
 

The following are the icon parameters.

<table>
<tr>
<th>Icon parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETICONMETRICS"></a><a id="spi_geticonmetrics"></a><dl>
<dt><b>SPI_GETICONMETRICS</b></dt>
<dt>0x002D</dt>
</dl>
</td>
<td width="60%">
Retrieves the metrics associated with icons. The <i>pvParam</i> parameter must point to an <a href="/windows/desktop/api/winuser/ns-winuser-iconmetricsa">ICONMETRICS</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(ICONMETRICS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETICONTITLELOGFONT"></a><a id="spi_geticontitlelogfont"></a><dl>
<dt><b>SPI_GETICONTITLELOGFONT</b></dt>
<dt>0x001F</dt>
</dl>
</td>
<td width="60%">
Retrieves the logical font information for the current icon-title font. The <i>uiParam</i> parameter specifies the size of a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure, and the <i>pvParam</i> parameter must point to the <b>LOGFONT</b> structure to fill in.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETICONTITLEWRAP"></a><a id="spi_geticontitlewrap"></a><dl>
<dt><b>SPI_GETICONTITLEWRAP</b></dt>
<dt>0x0019</dt>
</dl>
</td>
<td width="60%">
Determines whether icon-title wrapping is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_ICONHORIZONTALSPACING"></a><a id="spi_iconhorizontalspacing"></a><dl>
<dt><b>SPI_ICONHORIZONTALSPACING</b></dt>
<dt>0x000D</dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the width, in pixels, of an icon cell. The system uses this rectangle to arrange icons in large icon view.

To set this value, set <i>uiParam</i> to the new value and set <i>pvParam</i> to <b>NULL</b>. You cannot set this value to less than <b>SM_CXICON</b>.

To retrieve this value, <i>pvParam</i> must point to an integer that receives the  current value.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_ICONVERTICALSPACING"></a><a id="spi_iconverticalspacing"></a><dl>
<dt><b>SPI_ICONVERTICALSPACING</b></dt>
<dt>0x0018</dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the height, in pixels, of an icon cell.

To set this value, set <i>uiParam</i> to the new value and set <i>pvParam</i> to <b>NULL</b>. You cannot set this value to less than <b>SM_CYICON</b>.

To retrieve this value, <i>pvParam</i> must point to an integer that receives the  current value.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETICONMETRICS"></a><a id="spi_seticonmetrics"></a><dl>
<dt><b>SPI_SETICONMETRICS</b></dt>
<dt>0x002E</dt>
</dl>
</td>
<td width="60%">
Sets the metrics associated with icons. The <i>pvParam</i> parameter must point to an <a href="/windows/desktop/api/winuser/ns-winuser-iconmetricsa">ICONMETRICS</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(ICONMETRICS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETICONS"></a><a id="spi_seticons"></a><dl>
<dt><b>SPI_SETICONS</b></dt>
<dt>0x0058</dt>
</dl>
</td>
<td width="60%">
Reloads the system icons. Set the <i>uiParam</i> parameter to zero and the <i>pvParam</i> parameter to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETICONTITLELOGFONT"></a><a id="spi_seticontitlelogfont"></a><dl>
<dt><b>SPI_SETICONTITLELOGFONT</b></dt>
<dt>0x0022</dt>
</dl>
</td>
<td width="60%">
Sets the font that is used for icon titles. The <i>uiParam</i> parameter specifies the size of a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure, and the <i>pvParam</i> parameter must point to a <b>LOGFONT</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETICONTITLEWRAP"></a><a id="spi_seticontitlewrap"></a><dl>
<dt><b>SPI_SETICONTITLEWRAP</b></dt>
<dt>0x001A</dt>
</dl>
</td>
<td width="60%">
Turns icon-title wrapping on or off. The <i>uiParam</i> parameter specifies <b>TRUE</b> for on, or <b>FALSE</b> for off.

</td>
</tr>
</table>
 

The following are the input parameters. They include parameters related to the keyboard, mouse, pen, input language, and the warning beeper.

<table>
<tr>
<th>Input parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETBEEP"></a><a id="spi_getbeep"></a><dl>
<dt><b>SPI_GETBEEP</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Determines whether the warning beeper is on.

The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the beeper is on, or <b>FALSE</b> if it is off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETBLOCKSENDINPUTRESETS"></a><a id="spi_getblocksendinputresets"></a><dl>
<dt><b>SPI_GETBLOCKSENDINPUTRESETS</b></dt>
<dt>0x1026</dt>
</dl>
</td>
<td width="60%">
Retrieves a <b>BOOL</b> indicating whether an application can reset the screensaver's timer by calling the <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> function to simulate keyboard or mouse input. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the simulated input will be blocked, or <b>FALSE</b> otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETCONTACTVISUALIZATION"></a><a id="spi_getcontactvisualization"></a><dl>
<dt><b>SPI_GETCONTACTVISUALIZATION</b></dt>
<dt>0x2018</dt>
</dl>
</td>
<td width="60%">
Retrieves the current contact visualization setting. The <i>pvParam</i> parameter must point to a <b>ULONG</b> variable that receives the setting. For more information, see <a href="/windows/desktop/winmsg/contact-visualization">Contact Visualization</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETDEFAULTINPUTLANG"></a><a id="spi_getdefaultinputlang"></a><dl>
<dt><b>SPI_GETDEFAULTINPUTLANG</b></dt>
<dt>0x0059</dt>
</dl>
</td>
<td width="60%">
Retrieves the input locale identifier for the system default input language. The <i>pvParam</i> parameter must point to an <b>HKL</b> variable that receives this value. For more information, see <a href="/windows/desktop/inputdev/about-keyboard-input">Languages, Locales, and Keyboard Layouts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETGESTUREVISUALIZATION"></a><a id="spi_getgesturevisualization"></a><dl>
<dt><b>SPI_GETGESTUREVISUALIZATION</b></dt>
<dt>0x201A</dt>
</dl>
</td>
<td width="60%">
Retrieves the current gesture visualization setting. The <i>pvParam</i> parameter must point to a <b>ULONG</b> variable that receives the setting. For more information, see <a href="/windows/desktop/winmsg/gesture-visualization">Gesture Visualization</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETKEYBOARDCUES"></a><a id="spi_getkeyboardcues"></a><dl>
<dt><b>SPI_GETKEYBOARDCUES</b></dt>
<dt>0x100A</dt>
</dl>
</td>
<td width="60%">
Determines whether menu access keys are always underlined. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if menu access keys are always underlined, and <b>FALSE</b> if they are underlined only when the menu is activated by the keyboard.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETKEYBOARDDELAY"></a><a id="spi_getkeyboarddelay"></a><dl>
<dt><b>SPI_GETKEYBOARDDELAY</b></dt>
<dt>0x0016</dt>
</dl>
</td>
<td width="60%">
Retrieves the keyboard repeat-delay setting, which is a value in the range from 0 (approximately 250 ms delay) through 3 (approximately 1 second delay). The actual delay associated with each value may vary depending on the hardware. The <i>pvParam</i> parameter must point to an integer variable that receives the setting.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETKEYBOARDPREF"></a><a id="spi_getkeyboardpref"></a><dl>
<dt><b>SPI_GETKEYBOARDPREF</b></dt>
<dt>0x0044</dt>
</dl>
</td>
<td width="60%">
Determines whether the user relies on the keyboard instead of the mouse, and wants applications to display keyboard interfaces that would otherwise be hidden. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the user relies on the keyboard; or <b>FALSE</b> otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETKEYBOARDSPEED"></a><a id="spi_getkeyboardspeed"></a><dl>
<dt><b>SPI_GETKEYBOARDSPEED</b></dt>
<dt>0x000A</dt>
</dl>
</td>
<td width="60%">
Retrieves the keyboard repeat-speed setting, which is a value in the range from 0 (approximately 2.5 repetitions per second) through 31 (approximately 30 repetitions per second). The actual repeat rates are hardware-dependent and may vary from a linear scale by as much as 20%. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives the setting.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSE"></a><a id="spi_getmouse"></a><dl>
<dt><b>SPI_GETMOUSE</b></dt>
<dt>0x0003</dt>
</dl>
</td>
<td width="60%">
Retrieves the two mouse threshold values and the mouse acceleration. The <i>pvParam</i> parameter must point to an array of three integers that receives these values. See <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event">mouse_event</a> for further information.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSEHOVERHEIGHT"></a><a id="spi_getmousehoverheight"></a><dl>
<dt><b>SPI_GETMOUSEHOVERHEIGHT</b></dt>
<dt>0x0064</dt>
</dl>
</td>
<td width="60%">
Retrieves the height, in pixels, of the rectangle within which the mouse pointer has to stay for <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> to generate a <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> message. The <i>pvParam</i> parameter must point to a <b>UINT</b> variable that receives the height.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSEHOVERTIME"></a><a id="spi_getmousehovertime"></a><dl>
<dt><b>SPI_GETMOUSEHOVERTIME</b></dt>
<dt>0x0066</dt>
</dl>
</td>
<td width="60%">
Retrieves the time, in milliseconds, that the mouse pointer has to stay in the hover rectangle for <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> to generate a <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> message. The <i>pvParam</i> parameter must point to a <b>UINT</b> variable that receives the time.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSEHOVERWIDTH"></a><a id="spi_getmousehoverwidth"></a><dl>
<dt><b>SPI_GETMOUSEHOVERWIDTH</b></dt>
<dt>0x0062</dt>
</dl>
</td>
<td width="60%">
Retrieves the width, in pixels, of the rectangle within which the mouse pointer has to stay for <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> to generate a <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> message. The <i>pvParam</i> parameter must point to a <b>UINT</b> variable that receives the width.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSESPEED"></a><a id="spi_getmousespeed"></a><dl>
<dt><b>SPI_GETMOUSESPEED</b></dt>
<dt>0x0070</dt>
</dl>
</td>
<td width="60%">
Retrieves the current mouse speed. The mouse speed determines how far the pointer will move based on the distance the mouse moves. The <i>pvParam</i> parameter must point to an integer that receives a value which ranges between 1 (slowest) and 20 (fastest). A value of 10 is the default. The value can be set by an end-user using the mouse control panel application or by an application using <b>SPI_SETMOUSESPEED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSETRAILS"></a><a id="spi_getmousetrails"></a><dl>
<dt><b>SPI_GETMOUSETRAILS</b></dt>
<dt>0x005E</dt>
</dl>
</td>
<td width="60%">
Determines whether the Mouse Trails feature is enabled. This feature improves the visibility of mouse cursor movements by briefly showing a trail of cursors and quickly erasing them.

The <i>pvParam</i> parameter must point to an integer variable that receives a value. if  the value is zero or 1, the feature is disabled. If the value is greater than 1, the feature is enabled and the value indicates the number of cursors drawn in the trail. The <i>uiParam</i> parameter is not used.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSEWHEELROUTING"></a><a id="spi_getmousewheelrouting"></a><dl>
<dt><b>SPI_GETMOUSEWHEELROUTING</b></dt>
<dt>0x201C</dt>
</dl>
</td>
<td width="60%">
Retrieves the routing setting for wheel button input. The routing setting determines whether wheel button input is sent to the app with focus (foreground) or the app under the mouse cursor.

The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives the routing option. 
If  the value is zero or MOUSEWHEEL_ROUTING_FOCUS, mouse wheel input is delivered to the app with focus. If the value is 1 or MOUSEWHEEL_ROUTING_HYBRID (default), mouse wheel input is delivered to the app with focus (desktop apps) or the app under the mouse cursor (Windows Store apps).
The <i>uiParam</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETPENVISUALIZATION"></a><a id="spi_getpenvisualization"></a><dl>
<dt><b>SPI_GETPENVISUALIZATION</b></dt>
<dt>0x201E</dt>
</dl>
</td>
<td width="60%">
Retrieves the current pen gesture visualization setting. The <i>pvParam</i> parameter must point to a <b>ULONG</b> variable that receives the setting. For more information, see <a href="/windows/desktop/winmsg/pen-visualization">Pen Visualization</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSNAPTODEFBUTTON"></a><a id="spi_getsnaptodefbutton"></a><dl>
<dt><b>SPI_GETSNAPTODEFBUTTON</b></dt>
<dt>0x005F</dt>
</dl>
</td>
<td width="60%">
Determines whether the snap-to-default-button feature is enabled. If enabled, the mouse cursor automatically moves to the default button, such as <b>OK</b> or <b>Apply</b>, of a dialog box. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the feature is on, or <b>FALSE</b> if it is off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSYSTEMLANGUAGEBAR"></a><a id="spi_getsystemlanguagebar"></a><dl>
<dt><b>SPI_GETSYSTEMLANGUAGEBAR</b></dt>
<dt>0x1050</dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 8:</b> Determines whether the system language bar is enabled or disabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the language bar is enabled, or <b>FALSE</b> otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETTHREADLOCALINPUTSETTINGS"></a><a id="spi_getthreadlocalinputsettings"></a><dl>
<dt><b>SPI_GETTHREADLOCALINPUTSETTINGS</b></dt>
<dt>0x104E</dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 8:</b> Determines whether the active input settings have Local (per-thread, <b>TRUE</b>) or Global (session, <b>FALSE</b>) scope. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETTOUCHPADPARAMETERS"></a><a id="spi_gettouchpadparameters"></a><dl>
<dt><b>SPI_GETTOUCHPADPARAMETERS</b></dt>
<dt>0x00AE</dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 11, version 24H2:</b> Retrieves details about the Precision Touchpad, including user settings and system information related to the touchpad.

The *pvParam* parameter must point to a **[TOUCHPAD_PARAMETERS](/windows/win32/api/winuser/ns-winuser-touchpad_parameters)** structure.

The *uiParam* parameter must specify the size of the structure.

The value of the *versionNumber* field in the TOUCHPAD_PARAMETERS structure must be set to the appropriate value for the version of the structure being used.</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETWHEELSCROLLCHARS"></a><a id="spi_getwheelscrollchars"></a><dl>
<dt><b>SPI_GETWHEELSCROLLCHARS</b></dt>
<dt>0x006C</dt>
</dl>
</td>
<td width="60%">
Retrieves the number of characters to scroll when the horizontal mouse wheel is moved. The <i>pvParam</i> parameter must point to a <b>UINT</b> variable that receives the number of lines. The default value is 3.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETWHEELSCROLLLINES"></a><a id="spi_getwheelscrolllines"></a><dl>
<dt><b>SPI_GETWHEELSCROLLLINES</b></dt>
<dt>0x0068</dt>
</dl>
</td>
<td width="60%">
Retrieves the number of lines to scroll when the vertical mouse wheel is moved. The <i>pvParam</i> parameter must point to a <b>UINT</b> variable that receives the number of lines. The default value is 3.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETBEEP"></a><a id="spi_setbeep"></a><dl>
<dt><b>SPI_SETBEEP</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Turns the warning beeper on or off. The <i>uiParam</i> parameter specifies <b>TRUE</b> for on, or <b>FALSE</b> for off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETBLOCKSENDINPUTRESETS"></a><a id="spi_setblocksendinputresets"></a><dl>
<dt><b>SPI_SETBLOCKSENDINPUTRESETS</b></dt>
<dt>0x1027</dt>
</dl>
</td>
<td width="60%">
Determines whether an application can reset the screensaver's timer by calling the <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> function to simulate keyboard or mouse input. The <i>uiParam</i> parameter specifies <b>TRUE</b> if the screensaver will not be deactivated by simulated input, or <b>FALSE</b> if the screensaver will be deactivated by simulated input.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETCONTACTVISUALIZATION"></a><a id="spi_setcontactvisualization"></a><dl>
<dt><b>SPI_SETCONTACTVISUALIZATION</b></dt>
<dt>0x2019</dt>
</dl>
</td>
<td width="60%">
Sets the current contact visualization setting. The <i>pvParam</i> parameter must point to a <b>ULONG</b> variable that identifies the setting. For more information, see <a href="/windows/desktop/winmsg/contact-visualization">Contact Visualization</a>.

<div class="alert"><b>Note</b>  If contact visualizations are disabled, gesture visualizations cannot be enabled.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDEFAULTINPUTLANG"></a><a id="spi_setdefaultinputlang"></a><dl>
<dt><b>SPI_SETDEFAULTINPUTLANG</b></dt>
<dt>0x005A</dt>
</dl>
</td>
<td width="60%">
Sets the default input language for the system shell and applications. The specified language must be displayable using the current system character set. The <i>pvParam</i> parameter must point to an <b>HKL</b> variable that contains the input locale identifier for the default language. For more information, see <a href="/windows/desktop/inputdev/about-keyboard-input">Languages, Locales, and Keyboard Layouts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDOUBLECLICKTIME"></a><a id="spi_setdoubleclicktime"></a><dl>
<dt><b>SPI_SETDOUBLECLICKTIME</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Sets the double-click time for the mouse to the value of the <i>uiParam</i> parameter. If the <i>uiParam</i> value is greater than 5000 milliseconds, the system sets the double-click time to 5000 milliseconds.

The double-click time is the maximum number of milliseconds that can occur between the first and second clicks of a double-click. You can also call the <a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime">SetDoubleClickTime</a> function to set the double-click time. To get the current double-click time, call the <a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime">GetDoubleClickTime</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDOUBLECLKHEIGHT"></a><a id="spi_setdoubleclkheight"></a><dl>
<dt><b>SPI_SETDOUBLECLKHEIGHT</b></dt>
<dt>0x001E</dt>
</dl>
</td>
<td width="60%">
Sets the height of the double-click rectangle to the value of the <i>uiParam</i> parameter.

The double-click rectangle is the rectangle within which the second click of a double-click must fall for it to be registered as a double-click.

To retrieve the height of the double-click rectangle, call  <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with the <b>SM_CYDOUBLECLK</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDOUBLECLKWIDTH"></a><a id="spi_setdoubleclkwidth"></a><dl>
<dt><b>SPI_SETDOUBLECLKWIDTH</b></dt>
<dt>0x001D</dt>
</dl>
</td>
<td width="60%">
Sets the width of the double-click rectangle to the value of the <i>uiParam</i> parameter.

The double-click rectangle is the rectangle within which the second click of a double-click must fall for it to be registered as a double-click.

To retrieve the width of the double-click rectangle, call <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with the <b>SM_CXDOUBLECLK</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETGESTUREVISUALIZATION"></a><a id="spi_setgesturevisualization"></a><dl>
<dt><b>SPI_SETGESTUREVISUALIZATION</b></dt>
<dt>0x201B</dt>
</dl>
</td>
<td width="60%">
Sets the current gesture visualization setting. The <i>pvParam</i> parameter must point to a <b>ULONG</b> variable that identifies the setting. For more information, see <a href="/windows/desktop/winmsg/gesture-visualization">Gesture Visualization</a>.

<div class="alert"><b>Note</b>  If contact visualizations are disabled, gesture visualizations cannot be enabled.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETKEYBOARDCUES"></a><a id="spi_setkeyboardcues"></a><dl>
<dt><b>SPI_SETKEYBOARDCUES</b></dt>
<dt>0x100B</dt>
</dl>
</td>
<td width="60%">
Sets the underlining of menu access key letters. The <i>pvParam</i> parameter is a <b>BOOL</b> variable. Set <i>pvParam</i> to <b>TRUE</b> to always underline menu access keys, or <b>FALSE</b> to underline menu access keys only when the menu is activated from the keyboard.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETKEYBOARDDELAY"></a><a id="spi_setkeyboarddelay"></a><dl>
<dt><b>SPI_SETKEYBOARDDELAY</b></dt>
<dt>0x0017</dt>
</dl>
</td>
<td width="60%">
Sets the keyboard repeat-delay setting. The <i>uiParam</i> parameter must specify 0, 1, 2, or 3, where zero sets the shortest delay approximately 250 ms) and 3 sets the longest delay (approximately 1 second). The actual delay associated with each value may vary depending on the hardware.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETKEYBOARDPREF"></a><a id="spi_setkeyboardpref"></a><dl>
<dt><b>SPI_SETKEYBOARDPREF</b></dt>
<dt>0x0045</dt>
</dl>
</td>
<td width="60%">
Sets the keyboard preference. The <i>uiParam</i> parameter specifies <b>TRUE</b> if the user relies on the keyboard instead of the mouse, and wants applications to display keyboard interfaces that would otherwise be hidden; <i>uiParam</i> is <b>FALSE</b> otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETKEYBOARDSPEED"></a><a id="spi_setkeyboardspeed"></a><dl>
<dt><b>SPI_SETKEYBOARDSPEED</b></dt>
<dt>0x000B</dt>
</dl>
</td>
<td width="60%">
Sets the keyboard repeat-speed setting. The <i>uiParam</i> parameter must specify a value in the range from 0 (approximately 2.5 repetitions per second) through 31 (approximately 30 repetitions per second). The actual repeat rates are hardware-dependent and may vary from a linear scale by as much as 20%. If <i>uiParam</i> is greater than 31, the parameter is set to 31.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETLANGTOGGLE"></a><a id="spi_setlangtoggle"></a><dl>
<dt><b>SPI_SETLANGTOGGLE</b></dt>
<dt>0x005B</dt>
</dl>
</td>
<td width="60%">
Sets the hot key set for switching between input languages. The <i>uiParam</i> and <i>pvParam</i> parameters are not used. The value sets the shortcut keys in the keyboard property sheets by reading the registry again. The registry must be set before this flag is used. the path in the registry is 
                                    <b>HKEY_CURRENT_USER</b>&#92;<b>Keyboard Layout</b>&#92;<b>Toggle</b></p>. Valid values are "1" = ALT+SHIFT, "2" = CTRL+SHIFT, and "3" = none.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSE"></a><a id="spi_setmouse"></a><dl>
<dt><b>SPI_SETMOUSE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Sets the two mouse threshold values and the mouse acceleration. The <i>pvParam</i> parameter must point to an array of three integers that specifies these values. See <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event">mouse_event</a> for further information.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEBUTTONSWAP"></a><a id="spi_setmousebuttonswap"></a><dl>
<dt><b>SPI_SETMOUSEBUTTONSWAP</b></dt>
<dt>0x0021</dt>
</dl>
</td>
<td width="60%">
Swaps or restores the meaning of the left and right mouse buttons. The <i>uiParam</i> parameter specifies <b>TRUE</b> to swap the meanings of the buttons, or <b>FALSE</b> to restore their original meanings.

To retrieve the current setting, call <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with the <b>SM_SWAPBUTTON</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEHOVERHEIGHT"></a><a id="spi_setmousehoverheight"></a><dl>
<dt><b>SPI_SETMOUSEHOVERHEIGHT</b></dt>
<dt>0x0065</dt>
</dl>
</td>
<td width="60%">
Sets the height, in pixels, of the rectangle within which the mouse pointer has to stay for <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> to generate a <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> message. Set the <i>uiParam</i> parameter to the new height.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEHOVERTIME"></a><a id="spi_setmousehovertime"></a><dl>
<dt><b>SPI_SETMOUSEHOVERTIME</b></dt>
<dt>0x0067</dt>
</dl>
</td>
<td width="60%">
Sets the time, in milliseconds, that the mouse pointer has to stay in the hover rectangle for <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> to generate a <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> message. This is used only if you pass <b>HOVER_DEFAULT</b> in the <i>dwHoverTime</i> parameter in the call to <b>TrackMouseEvent</b>. Set the <i>uiParam</i> parameter to the new time.

The time specified should be between <b>USER_TIMER_MAXIMUM</b> and <b>USER_TIMER_MINIMUM</b>. If <i>uiParam</i> is less than <b>USER_TIMER_MINIMUM</b>, the function will use <b>USER_TIMER_MINIMUM</b>. If <i>uiParam</i> is greater than <b>USER_TIMER_MAXIMUM</b>, the function will be <b>USER_TIMER_MAXIMUM</b>.               

<b>Windows Server 2003 and Windows XP:  </b>The operating system does not enforce the use of <b>USER_TIMER_MAXIMUM</b> and <b>USER_TIMER_MINIMUM</b> until Windows Server 2003 with SP1 and Windows XP with SP2.



</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEHOVERWIDTH"></a><a id="spi_setmousehoverwidth"></a><dl>
<dt><b>SPI_SETMOUSEHOVERWIDTH</b></dt>
<dt>0x0063</dt>
</dl>
</td>
<td width="60%">
Sets the width, in pixels, of the rectangle within which the mouse pointer has to stay for <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> to generate a <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> message. Set the <i>uiParam</i> parameter to the new width.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSESPEED"></a><a id="spi_setmousespeed"></a><dl>
<dt><b>SPI_SETMOUSESPEED</b></dt>
<dt>0x0071</dt>
</dl>
</td>
<td width="60%">
Sets the current mouse speed. The <i>pvParam</i> parameter is an integer between 1 (slowest) and 20 (fastest). A value of 10 is the default. This value is typically set using the mouse control panel application.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSETRAILS"></a><a id="spi_setmousetrails"></a><dl>
<dt><b>SPI_SETMOUSETRAILS</b></dt>
<dt>0x005D</dt>
</dl>
</td>
<td width="60%">
Enables or disables the Mouse Trails feature, which improves the visibility of mouse cursor movements by briefly showing a trail of cursors and quickly erasing them.

To disable the feature, set the <i>uiParam</i> parameter to zero or 1. To enable the  feature, set <i>uiParam</i> to a value greater than 1 to indicate the number of cursors drawn in the trail.

<b>Windows 2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEWHEELROUTING"></a><a id="spi_setmousewheelrouting"></a><dl>
<dt><b>SPI_SETMOUSEWHEELROUTING</b></dt>
<dt>0x201D</dt>
</dl>
</td>
<td width="60%">
Sets the routing setting for wheel button input. The routing setting determines whether wheel button input is sent to the app with focus (foreground) or the app under the mouse cursor.

The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives the routing option. 
If  the value is zero or MOUSEWHEEL_ROUTING_FOCUS, mouse wheel input is delivered to the app with focus. If the value is 1 or MOUSEWHEEL_ROUTING_HYBRID (default), mouse wheel input is delivered to the app with focus (desktop apps) or the app under the mouse cursor (Windows Store apps).
Set the <i>uiParam</i> parameter to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETPENVISUALIZATION"></a><a id="spi_setpenvisualization"></a><dl>
<dt><b>SPI_SETPENVISUALIZATION</b></dt>
<dt>0x201F</dt>
</dl>
</td>
<td width="60%">
Sets the current pen gesture visualization setting. The <i>pvParam</i> parameter must point to a <b>ULONG</b> variable that identifies the setting. For more information, see <a href="/windows/desktop/winmsg/pen-visualization">Pen Visualization</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSNAPTODEFBUTTON"></a><a id="spi_setsnaptodefbutton"></a><dl>
<dt><b>SPI_SETSNAPTODEFBUTTON</b></dt>
<dt>0x0060</dt>
</dl>
</td>
<td width="60%">
Enables or disables the snap-to-default-button feature. If enabled, the mouse cursor automatically moves to the default button, such as <b>OK</b> or <b>Apply</b>, of a dialog box. Set the <i>uiParam</i> parameter to <b>TRUE</b> to enable the feature, or <b>FALSE</b> to disable it. Applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function when displaying a dialog box so the dialog manager can position the mouse cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSYSTEMLANGUAGEBAR"></a><a id="spi_setsystemlanguagebar"></a><dl>
<dt><b>SPI_SETSYSTEMLANGUAGEBAR</b></dt>
<dt>0x1051</dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 8:</b> Turns the legacy language bar feature on or off. The <i>pvParam</i> parameter is a pointer to a <b>BOOL</b> variable. Set <i>pvParam</i> to <b>TRUE</b> to enable the legacy language bar, or <b>FALSE</b> to disable it. The flag is supported on Windows 8 where the legacy language bar is replaced by Input Switcher and therefore turned off by default. Turning the legacy language bar on is provided for compatibility reasons and has no effect on the Input Switcher.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETTHREADLOCALINPUTSETTINGS"></a><a id="spi_setthreadlocalinputsettings"></a><dl>
<dt><b>SPI_SETTHREADLOCALINPUTSETTINGS</b></dt>
<dt>0x104F</dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 8:</b> Determines whether the active input settings have Local (per-thread, <b>TRUE</b>) or Global (session, <b>FALSE</b>) scope. The <i>pvParam</i> parameter must be a <b>BOOL</b> variable, casted by PVOID.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETTOUCHPADPARAMETERS"></a><a id="spi_settouchpadparameters"></a><dl>
<dt><b>SPI_SETTOUCHPADPARAMETERS</b></dt>
<dt>0x00AF</dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 11, version 24H2:</b> Sets details about the Precision Touchpad, including user settings and system information related to the touchpad.

The *pvParam* parameter must point to a **[TOUCHPAD_PARAMETERS](/windows/win32/api/winuser/ns-winuser-touchpad_parameters)** structure.

The *uiParam* parameter must specify the size of the structure.

The value of the *versionNumber* field in the TOUCHPAD_PARAMETERS structure must be set to the appropriate value for the version of the structure being used.
</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETWHEELSCROLLCHARS"></a><a id="spi_setwheelscrollchars"></a><dl>
<dt><b>SPI_SETWHEELSCROLLCHARS</b></dt>
<dt>0x006D</dt>
</dl>
</td>
<td width="60%">
Sets the number of characters to scroll when the horizontal mouse wheel is moved. The number of characters is set from the <i>uiParam</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETWHEELSCROLLLINES"></a><a id="spi_setwheelscrolllines"></a><dl>
<dt><b>SPI_SETWHEELSCROLLLINES</b></dt>
<dt>0x0069</dt>
</dl>
</td>
<td width="60%">
Sets the number of lines to scroll when the vertical mouse wheel is moved. The number of lines is set from the <i>uiParam</i> parameter.

The number of lines is the suggested number of lines to scroll when the mouse wheel is rolled without using modifier keys. If the number is 0, then no scrolling should occur. If the number of lines to scroll is  greater than the number of lines viewable, and in particular if it is <b>WHEEL_PAGESCROLL</b> (#defined as <b>UINT_MAX</b>), the scroll operation should be interpreted as clicking once in the page down or page up regions of the scroll bar.

</td>
</tr>
</table>
 

The following are the menu parameters.

<table>
<tr>
<th>Menu parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMENUDROPALIGNMENT"></a><a id="spi_getmenudropalignment"></a><dl>
<dt><b>SPI_GETMENUDROPALIGNMENT</b></dt>
<dt>0x001B</dt>
</dl>
</td>
<td width="60%">
Determines whether pop-up menus are left-aligned or right-aligned, relative to the corresponding menu-bar item. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if right-aligned, or <b>FALSE</b> otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMENUFADE"></a><a id="spi_getmenufade"></a><dl>
<dt><b>SPI_GETMENUFADE</b></dt>
<dt>0x1012</dt>
</dl>
</td>
<td width="60%">
Determines whether menu fade animation is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> when fade animation is enabled and <b>FALSE</b> when it isdisabled. If fade animation is disabled, menus use slide animation. This flag is ignored unless menu animation is enabled, which you can do using the <b>SPI_SETMENUANIMATION</b> flag. For more information, see <a href="/windows/desktop/api/winuser/nf-winuser-animatewindow">AnimateWindow</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMENUSHOWDELAY"></a><a id="spi_getmenushowdelay"></a><dl>
<dt><b>SPI_GETMENUSHOWDELAY</b></dt>
<dt>0x006A</dt>
</dl>
</td>
<td width="60%">
Retrieves the time, in milliseconds, that the system waits before displaying a shortcut menu when the mouse cursor is over a submenu item. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives the time of the delay.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMENUDROPALIGNMENT"></a><a id="spi_setmenudropalignment"></a><dl>
<dt><b>SPI_SETMENUDROPALIGNMENT</b></dt>
<dt>0x001C</dt>
</dl>
</td>
<td width="60%">
Sets the alignment value of pop-up menus. The <i>uiParam</i> parameter specifies <b>TRUE</b> for right alignment, or <b>FALSE</b> for left alignment.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMENUFADE"></a><a id="spi_setmenufade"></a><dl>
<dt><b>SPI_SETMENUFADE</b></dt>
<dt>0x1013</dt>
</dl>
</td>
<td width="60%">
Enables or disables menu fade animation. Set <i>pvParam</i> to <b>TRUE</b> to enable the menu fade effect or <b>FALSE</b> to disable it. If fade animation is disabled, menus use slide animation. he The menu fade effect is possible only if the system has a color depth of more than 256 colors. This flag is ignored unless <b>SPI_MENUANIMATION</b> is also set. For more information, see <a href="/windows/desktop/api/winuser/nf-winuser-animatewindow">AnimateWindow</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMENUSHOWDELAY"></a><a id="spi_setmenushowdelay"></a><dl>
<dt><b>SPI_SETMENUSHOWDELAY</b></dt>
<dt>0x006B</dt>
</dl>
</td>
<td width="60%">
Sets <i>uiParam</i> to the time, in milliseconds, that the system waits before displaying a shortcut menu when the mouse cursor is over a submenu item.

</td>
</tr>
</table>
 

The following are the power parameters.

Beginning with Windows Server 2008 and Windows Vista, these power parameters are not supported. Instead, to determine the current display power state, an application should register for <b>GUID_MONITOR_POWER_STATE</b> notifications. To determine the current display power down time-out, an application should register for notification of changes to the <b>GUID_VIDEO_POWERDOWN_TIMEOUT</b> power setting. For more information, see <a href="/windows/desktop/Power/registering-for-power-events">Registering for Power Events</a>.

<b>Windows Server 2003 and Windows XP/2000:  </b>To determine the current display power state, use the following power parameters.

<table>
<tr>
<th>Power parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETLOWPOWERACTIVE"></a><a id="spi_getlowpoweractive"></a><dl>
<dt><b>SPI_GETLOWPOWERACTIVE</b></dt>
<dt>0x0053</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported.

<b>Windows Server 2003 and Windows XP/2000:  </b>Determines whether the low-power phase of screen saving is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> if disabled. This flag is supported for 32-bit applications only.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETLOWPOWERTIMEOUT"></a><a id="spi_getlowpowertimeout"></a><dl>
<dt><b>SPI_GETLOWPOWERTIMEOUT</b></dt>
<dt>0x004F</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported.

<b>Windows Server 2003 and Windows XP/2000:  </b>Retrieves the time-out value for the low-power phase of screen saving. The <i>pvParam</i> parameter must point to an integer variable that receives the value. This flag is supported for 32-bit applications only.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETPOWEROFFACTIVE"></a><a id="spi_getpoweroffactive"></a><dl>
<dt><b>SPI_GETPOWEROFFACTIVE</b></dt>
<dt>0x0054</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported. When the power-off phase of screen saving is enabled, the <b>GUID_VIDEO_POWERDOWN_TIMEOUT</b> power setting is greater than zero.

<b>Windows Server 2003 and Windows XP/2000:  </b>Determines whether the power-off phase of screen saving is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> if disabled. This flag is supported for 32-bit applications only.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETPOWEROFFTIMEOUT"></a><a id="spi_getpowerofftimeout"></a><dl>
<dt><b>SPI_GETPOWEROFFTIMEOUT</b></dt>
<dt>0x0050</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported. Instead, check the <b>GUID_VIDEO_POWERDOWN_TIMEOUT</b> power setting.

<b>Windows Server 2003 and Windows XP/2000:  </b>Retrieves the time-out value for the power-off phase of screen saving. The <i>pvParam</i> parameter must point to an integer variable that receives the value. This flag is supported for 32-bit applications only.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETLOWPOWERACTIVE"></a><a id="spi_setlowpoweractive"></a><dl>
<dt><b>SPI_SETLOWPOWERACTIVE</b></dt>
<dt>0x0055</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported.

<b>Windows Server 2003 and Windows XP/2000:  </b>Activates or deactivates the low-power phase of screen saving. Set <i>uiParam</i> to 1 to activate, or zero to deactivate. The <i>pvParam</i> parameter must be <b>NULL</b>. This flag is supported for 32-bit applications only.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETLOWPOWERTIMEOUT"></a><a id="spi_setlowpowertimeout"></a><dl>
<dt><b>SPI_SETLOWPOWERTIMEOUT</b></dt>
<dt>0x0051</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported.

<b>Windows Server 2003 and Windows XP/2000:  </b>Sets the time-out value, in seconds, for the low-power phase of screen saving. The <i>uiParam</i> parameter specifies the new value. The <i>pvParam</i> parameter must be <b>NULL</b>. This flag is supported for 32-bit applications only.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETPOWEROFFACTIVE"></a><a id="spi_setpoweroffactive"></a><dl>
<dt><b>SPI_SETPOWEROFFACTIVE</b></dt>
<dt>0x0056</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported. Instead, set the <b>GUID_VIDEO_POWERDOWN_TIMEOUT</b> power setting.

<b>Windows Server 2003 and Windows XP/2000:  </b>Activates or deactivates the power-off phase of screen saving. Set <i>uiParam</i> to 1 to activate, or zero to deactivate. The <i>pvParam</i> parameter must be <b>NULL</b>. This flag is supported for 32-bit applications only.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETPOWEROFFTIMEOUT"></a><a id="spi_setpowerofftimeout"></a><dl>
<dt><b>SPI_SETPOWEROFFTIMEOUT</b></dt>
<dt>0x0052</dt>
</dl>
</td>
<td width="60%">
This parameter is not supported. Instead, set the <b>GUID_VIDEO_POWERDOWN_TIMEOUT</b> power setting to a time-out value.

<b>Windows Server 2003 and Windows XP/2000:  </b>Sets the time-out value, in seconds, for the power-off phase of screen saving. The <i>uiParam</i> parameter specifies the new value. The <i>pvParam</i> parameter must be <b>NULL</b>. This flag is supported for 32-bit applications only.

</td>
</tr>
</table>
 

The following are the screen saver parameters.

<table>
<tr>
<th>Screen saver parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSCREENSAVEACTIVE"></a><a id="spi_getscreensaveactive"></a><dl>
<dt><b>SPI_GETSCREENSAVEACTIVE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Determines whether screen saving is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if screen saving is enabled, or <b>FALSE</b> otherwise.

<b>Windows 7, Windows Server 2008 R2 and Windows 2000:  </b>The function returns <b>TRUE</b> even when screen saving is not enabled. 

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSCREENSAVERRUNNING"></a><a id="spi_getscreensaverrunning"></a><dl>
<dt><b>SPI_GETSCREENSAVERRUNNING</b></dt>
<dt>0x0072</dt>
</dl>
</td>
<td width="60%">
Determines whether a screen saver is currently running on the window station of the calling process. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if a screen saver is currently running, or <b>FALSE</b> otherwise. Note that only the interactive window station, WinSta0, can have a screen saver running.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSCREENSAVESECURE"></a><a id="spi_getscreensavesecure"></a><dl>
<dt><b>SPI_GETSCREENSAVESECURE</b></dt>
<dt>0x0076</dt>
</dl>
</td>
<td width="60%">
Determines whether the screen saver  requires a password to display the Windows desktop. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the screen saver requires a password, or <b>FALSE</b> otherwise. The <i>uiParam</i> parameter is ignored.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSCREENSAVETIMEOUT"></a><a id="spi_getscreensavetimeout"></a><dl>
<dt><b>SPI_GETSCREENSAVETIMEOUT</b></dt>
<dt>0x000E</dt>
</dl>
</td>
<td width="60%">
Retrieves the screen saver time-out value, in seconds. The <i>pvParam</i> parameter must point to an integer variable that receives the value.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSCREENSAVEACTIVE"></a><a id="spi_setscreensaveactive"></a><dl>
<dt><b>SPI_SETSCREENSAVEACTIVE</b></dt>
<dt>0x0011</dt>
</dl>
</td>
<td width="60%">
Sets the state of the screen saver. The <i>uiParam</i> parameter specifies <b>TRUE</b> to activate screen saving, or <b>FALSE</b> to deactivate it.

If the machine has entered power saving mode or system lock state, an ERROR_OPERATION_IN_PROGRESS exception occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSCREENSAVESECURE"></a><a id="spi_setscreensavesecure"></a><dl>
<dt><b>SPI_SETSCREENSAVESECURE</b></dt>
<dt>0x0077</dt>
</dl>
</td>
<td width="60%">
Sets whether the screen saver requires the user to enter a password to display the Windows desktop. The <i>uiParam</i> parameter is a <b>BOOL</b> variable. The <i>pvParam</i> parameter is ignored. Set <i>uiParam</i> to <b>TRUE</b> to require a password, or <b>FALSE</b> to not require a password.

If the machine has entered power saving mode or system lock state, an ERROR_OPERATION_IN_PROGRESS exception occurs.

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSCREENSAVETIMEOUT"></a><a id="spi_setscreensavetimeout"></a><dl>
<dt><b>SPI_SETSCREENSAVETIMEOUT</b></dt>
<dt>0x000F</dt>
</dl>
</td>
<td width="60%">
Sets the screen saver time-out value to the value of the <i>uiParam</i> parameter. This value is the amount of time, in seconds, that the system must be idle before the screen saver activates.

If the machine has entered power saving mode or system lock state, an ERROR_OPERATION_IN_PROGRESS exception occurs.

</td>
</tr>
</table>
 

The following are the time-out parameters for applications and services.

<table>
<tr>
<th>Time-out parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETHUNGAPPTIMEOUT"></a><a id="spi_gethungapptimeout"></a><dl>
<dt><b>SPI_GETHUNGAPPTIMEOUT</b></dt>
<dt>0x0078</dt>
</dl>
</td>
<td width="60%">
Retrieves the number of milliseconds that a thread can go without dispatching a message before the system considers it unresponsive. The <i>pvParam</i> parameter must point to an integer variable that receives the value.

                                

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETWAITTOKILLTIMEOUT"></a><a id="spi_getwaittokilltimeout"></a><dl>
<dt><b>SPI_GETWAITTOKILLTIMEOUT</b></dt>
<dt>0x007A</dt>
</dl>
</td>
<td width="60%">
Retrieves the number of milliseconds that the system waits before terminating an application that does not respond to a shutdown request. The <i>pvParam</i> parameter must point to an integer variable that receives the value.

                                

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETWAITTOKILLSERVICETIMEOUT"></a><a id="spi_getwaittokillservicetimeout"></a><dl>
<dt><b>SPI_GETWAITTOKILLSERVICETIMEOUT</b></dt>
<dt>0x007C</dt>
</dl>
</td>
<td width="60%">
Retrieves the number of milliseconds that the service control manager waits before terminating a service that does not respond to a shutdown request. The <i>pvParam</i> parameter must point to an integer variable that receives the value.

                                

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETHUNGAPPTIMEOUT"></a><a id="spi_sethungapptimeout"></a><dl>
<dt><b>SPI_SETHUNGAPPTIMEOUT</b></dt>
<dt>0x0079</dt>
</dl>
</td>
<td width="60%">
Sets the hung application time-out to the value of the <i>uiParam</i> parameter. This value is the number of milliseconds that a thread can go without dispatching a message before the system considers it unresponsive.
                    
                                

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETWAITTOKILLTIMEOUT"></a><a id="spi_setwaittokilltimeout"></a><dl>
<dt><b>SPI_SETWAITTOKILLTIMEOUT</b></dt>
<dt>0x007B</dt>
</dl>
</td>
<td width="60%">
Sets the application shutdown request time-out to the value of the <i>uiParam</i> parameter. This value is the number of milliseconds that the system waits before terminating an application that does not respond to a shutdown request.

                                

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETWAITTOKILLSERVICETIMEOUT"></a><a id="spi_setwaittokillservicetimeout"></a><dl>
<dt><b>SPI_SETWAITTOKILLSERVICETIMEOUT</b></dt>
<dt>0x007D</dt>
</dl>
</td>
<td width="60%">
Sets the service shutdown request time-out to the value of the <i>uiParam</i> parameter. This value is the number of milliseconds that the system waits before terminating a service that does not respond to a shutdown request.
                                

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
</table>
 

The following are the UI effects. The <b>SPI_SETUIEFFECTS</b> value is used to enable or disable all UI effects at once. This table contains the complete list of UI effect values.

<table>
<tr>
<th>UI effects parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETCOMBOBOXANIMATION"></a><a id="spi_getcomboboxanimation"></a><dl>
<dt><b>SPI_GETCOMBOBOXANIMATION</b></dt>
<dt>0x1004</dt>
</dl>
</td>
<td width="60%">
Determines whether the slide-open effect for combo boxes is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> for enabled, or <b>FALSE</b> for disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETCURSORSHADOW"></a><a id="spi_getcursorshadow"></a><dl>
<dt><b>SPI_GETCURSORSHADOW</b></dt>
<dt>0x101A</dt>
</dl>
</td>
<td width="60%">
Determines whether the cursor has a shadow around it. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the shadow is enabled, <b>FALSE</b> if it is disabled. This effect appears only if the system has a color depth of more than 256 colors.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETGRADIENTCAPTIONS"></a><a id="spi_getgradientcaptions"></a><dl>
<dt><b>SPI_GETGRADIENTCAPTIONS</b></dt>
<dt>0x1008</dt>
</dl>
</td>
<td width="60%">
Determines whether the gradient effect for window title bars is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> for enabled, or <b>FALSE</b> for disabled. For more information about the gradient effect, see the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETHOTTRACKING"></a><a id="spi_gethottracking"></a><dl>
<dt><b>SPI_GETHOTTRACKING</b></dt>
<dt>0x100E</dt>
</dl>
</td>
<td width="60%">
Determines whether hot tracking of user-interface elements, such as menu names on menu bars, is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> for enabled, or <b>FALSE</b> for disabled.

Hot tracking means that when the cursor moves over an item, it is highlighted but not selected. You can query this value to decide whether to use hot tracking in the user interface of your application.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETLISTBOXSMOOTHSCROLLING"></a><a id="spi_getlistboxsmoothscrolling"></a><dl>
<dt><b>SPI_GETLISTBOXSMOOTHSCROLLING</b></dt>
<dt>0x1006</dt>
</dl>
</td>
<td width="60%">
Determines whether the smooth-scrolling effect for list boxes is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> for enabled, or <b>FALSE</b> for disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMENUANIMATION"></a><a id="spi_getmenuanimation"></a><dl>
<dt><b>SPI_GETMENUANIMATION</b></dt>
<dt>0x1002</dt>
</dl>
</td>
<td width="60%">
Determines whether the menu animation feature is enabled. This master switch must be on to enable menu animation effects. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if animation is enabled and <b>FALSE</b> if it is disabled.

If animation is enabled, <b>SPI_GETMENUFADE</b> indicates whether menus use fade or slide animation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMENUUNDERLINES"></a><a id="spi_getmenuunderlines"></a><dl>
<dt><b>SPI_GETMENUUNDERLINES</b></dt>
<dt>0x100A</dt>
</dl>
</td>
<td width="60%">
Same as <b>SPI_GETKEYBOARDCUES</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSELECTIONFADE"></a><a id="spi_getselectionfade"></a><dl>
<dt><b>SPI_GETSELECTIONFADE</b></dt>
<dt>0x1014</dt>
</dl>
</td>
<td width="60%">
Determines whether the selection fade effect is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled or <b>FALSE</b> if disabled.

The selection fade effect causes the menu item selected by the user to remain on the screen briefly while fading out after the menu is dismissed.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETTOOLTIPANIMATION"></a><a id="spi_gettooltipanimation"></a><dl>
<dt><b>SPI_GETTOOLTIPANIMATION</b></dt>
<dt>0x1016</dt>
</dl>
</td>
<td width="60%">
Determines whether ToolTip animation is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled or <b>FALSE</b> if disabled. If ToolTip animation is enabled, <b>SPI_GETTOOLTIPFADE</b> indicates whether ToolTips use fade or slide animation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETTOOLTIPFADE"></a><a id="spi_gettooltipfade"></a><dl>
<dt><b>SPI_GETTOOLTIPFADE</b></dt>
<dt>0x1018</dt>
</dl>
</td>
<td width="60%">
If <b>SPI_SETTOOLTIPANIMATION</b> is enabled, <b>SPI_GETTOOLTIPFADE</b> indicates whether ToolTip animation uses a fade effect or a slide effect. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> for fade animation or <b>FALSE</b> for slide animation. For more information on slide and fade effects, see <a href="/windows/desktop/api/winuser/nf-winuser-animatewindow">AnimateWindow</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETUIEFFECTS"></a><a id="spi_getuieffects"></a><dl>
<dt><b>SPI_GETUIEFFECTS</b></dt>
<dt>0x103E</dt>
</dl>
</td>
<td width="60%">
Determines whether UI effects are enabled or disabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if all UI effects are enabled, or <b>FALSE</b> if they are disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETCOMBOBOXANIMATION"></a><a id="spi_setcomboboxanimation"></a><dl>
<dt><b>SPI_SETCOMBOBOXANIMATION</b></dt>
<dt>0x1005</dt>
</dl>
</td>
<td width="60%">
Enables or disables the slide-open effect for combo boxes. Set the <i>pvParam</i> parameter to <b>TRUE</b> to enable the gradient effect, or <b>FALSE</b> to disable it.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETCURSORSHADOW"></a><a id="spi_setcursorshadow"></a><dl>
<dt><b>SPI_SETCURSORSHADOW</b></dt>
<dt>0x101B</dt>
</dl>
</td>
<td width="60%">
Enables or disables a shadow around the cursor. The <i>pvParam</i> parameter is a <b>BOOL</b> variable. Set <i>pvParam</i> to <b>TRUE</b> to enable the shadow or <b>FALSE</b> to disable the shadow. This effect appears only if the system has a color depth of more than 256 colors.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETGRADIENTCAPTIONS"></a><a id="spi_setgradientcaptions"></a><dl>
<dt><b>SPI_SETGRADIENTCAPTIONS</b></dt>
<dt>0x1009</dt>
</dl>
</td>
<td width="60%">
Enables or disables the gradient effect for window title bars. Set the <i>pvParam</i> parameter to <b>TRUE</b> to enable it, or <b>FALSE</b> to disable it. The gradient effect is possible only if the system has a color depth of more than 256 colors. For more information about the gradient effect, see the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETHOTTRACKING"></a><a id="spi_sethottracking"></a><dl>
<dt><b>SPI_SETHOTTRACKING</b></dt>
<dt>0x100F</dt>
</dl>
</td>
<td width="60%">
Enables or disables hot tracking of user-interface elements such as menu names on menu bars. Set the <i>pvParam</i> parameter to <b>TRUE</b> to enable it, or <b>FALSE</b> to disable it.

Hot-tracking means that when the cursor moves over an item, it is highlighted but not selected.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETLISTBOXSMOOTHSCROLLING"></a><a id="spi_setlistboxsmoothscrolling"></a><dl>
<dt><b>SPI_SETLISTBOXSMOOTHSCROLLING</b></dt>
<dt>0x1007</dt>
</dl>
</td>
<td width="60%">
Enables or disables the smooth-scrolling effect for list boxes. Set the <i>pvParam</i> parameter to <b>TRUE</b> to enable the smooth-scrolling effect, or <b>FALSE</b> to disable it.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMENUANIMATION"></a><a id="spi_setmenuanimation"></a><dl>
<dt><b>SPI_SETMENUANIMATION</b></dt>
<dt>0x1003</dt>
</dl>
</td>
<td width="60%">
Enables or disables menu animation. This master switch must be on for any menu animation to occur. The <i>pvParam</i> parameter is a <b>BOOL</b> variable; set <i>pvParam</i> to <b>TRUE</b> to enable animation and <b>FALSE</b> to disable animation.

If animation is enabled, <b>SPI_GETMENUFADE</b> indicates whether menus use fade or slide animation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMENUUNDERLINES"></a><a id="spi_setmenuunderlines"></a><dl>
<dt><b>SPI_SETMENUUNDERLINES</b></dt>
<dt>0x100B</dt>
</dl>
</td>
<td width="60%">
Same as <b>SPI_SETKEYBOARDCUES</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSELECTIONFADE"></a><a id="spi_setselectionfade"></a><dl>
<dt><b>SPI_SETSELECTIONFADE</b></dt>
<dt>0x1015</dt>
</dl>
</td>
<td width="60%">
Set <i>pvParam</i> to <b>TRUE</b> to enable the selection fade effect or <b>FALSE</b> to disable it.

The selection fade effect causes the menu item selected by the user to remain on the screen briefly while fading out after the menu is dismissed. The selection fade effect is possible only if the system has a color depth of more than 256 colors.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETTOOLTIPANIMATION"></a><a id="spi_settooltipanimation"></a><dl>
<dt><b>SPI_SETTOOLTIPANIMATION</b></dt>
<dt>0x1017</dt>
</dl>
</td>
<td width="60%">
Set <i>pvParam</i> to <b>TRUE</b> to enable ToolTip animation or <b>FALSE</b> to disable it. If enabled, you can use <b>SPI_SETTOOLTIPFADE</b> to specify fade or slide animation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETTOOLTIPFADE"></a><a id="spi_settooltipfade"></a><dl>
<dt><b>SPI_SETTOOLTIPFADE</b></dt>
<dt>0x1019</dt>
</dl>
</td>
<td width="60%">
If the <b>SPI_SETTOOLTIPANIMATION</b> flag is enabled, use <b>SPI_SETTOOLTIPFADE</b> to indicate whether ToolTip animation uses a fade effect or a slide effect. Set <i>pvParam</i> to <b>TRUE</b> for fade animation or <b>FALSE</b> for slide animation. The tooltip fade effect is possible only if the system has a color depth of more than 256 colors. For more information on the slide and fade effects, see the <a href="/windows/desktop/api/winuser/nf-winuser-animatewindow">AnimateWindow</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETUIEFFECTS"></a><a id="spi_setuieffects"></a><dl>
<dt><b>SPI_SETUIEFFECTS</b></dt>
<dt>0x103F</dt>
</dl>
</td>
<td width="60%">
Enables or disables UI effects. Set the <i>pvParam</i> parameter to <b>TRUE</b> to enable all UI effects or <b>FALSE</b> to disable all UI effects.

</td>
</tr>
</table>
 

The following are the window parameters.

<table>
<tr>
<th>Window parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPI_GETACTIVEWINDOWTRACKING"></a><a id="spi_getactivewindowtracking"></a><dl>
<dt><b>SPI_GETACTIVEWINDOWTRACKING</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Determines whether active window tracking (activating the window the mouse is on) is on or off. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> for on, or <b>FALSE</b> for off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETACTIVEWNDTRKZORDER"></a><a id="spi_getactivewndtrkzorder"></a><dl>
<dt><b>SPI_GETACTIVEWNDTRKZORDER</b></dt>
<dt>0x100C</dt>
</dl>
</td>
<td width="60%">
Determines whether windows activated through active window tracking will be brought to the top. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> for on, or <b>FALSE</b> for off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETACTIVEWNDTRKTIMEOUT"></a><a id="spi_getactivewndtrktimeout"></a><dl>
<dt><b>SPI_GETACTIVEWNDTRKTIMEOUT</b></dt>
<dt>0x2002</dt>
</dl>
</td>
<td width="60%">
Retrieves the active window tracking delay, in milliseconds. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives the time.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETANIMATION"></a><a id="spi_getanimation"></a><dl>
<dt><b>SPI_GETANIMATION</b></dt>
<dt>0x0048</dt>
</dl>
</td>
<td width="60%">
Retrieves the animation effects associated with user actions. The <i>pvParam</i> parameter must point to an <a href="/windows/desktop/api/winuser/ns-winuser-animationinfo">ANIMATIONINFO</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(ANIMATIONINFO)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETBORDER"></a><a id="spi_getborder"></a><dl>
<dt><b>SPI_GETBORDER</b></dt>
<dt>0x0005</dt>
</dl>
</td>
<td width="60%">
Retrieves the border multiplier factor that determines the width of a window's sizing border. The <i>pvParam</i> parameter must point to an integer variable that receives this value.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETCARETWIDTH"></a><a id="spi_getcaretwidth"></a><dl>
<dt><b>SPI_GETCARETWIDTH</b></dt>
<dt>0x2006</dt>
</dl>
</td>
<td width="60%">
Retrieves the caret width in edit controls, in pixels. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives this value.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETDOCKMOVING"></a><a id="spi_getdockmoving"></a><dl>
<dt><b>SPI_GETDOCKMOVING</b></dt>
<dt>0x0090</dt>
</dl>
</td>
<td width="60%">
Determines whether a window is docked when it is moved to the top, left, or right edges of a monitor or monitor array. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> otherwise.

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETDRAGFROMMAXIMIZE"></a><a id="spi_getdragfrommaximize"></a><dl>
<dt><b>SPI_GETDRAGFROMMAXIMIZE</b></dt>
<dt>0x008C</dt>
</dl>
</td>
<td width="60%">
Determines whether a maximized window is restored when its caption bar is dragged. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> otherwise.

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETDRAGFULLWINDOWS"></a><a id="spi_getdragfullwindows"></a><dl>
<dt><b>SPI_GETDRAGFULLWINDOWS</b></dt>
<dt>0x0026</dt>
</dl>
</td>
<td width="60%">
Determines whether dragging of full windows is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFOREGROUNDFLASHCOUNT"></a><a id="spi_getforegroundflashcount"></a><dl>
<dt><b>SPI_GETFOREGROUNDFLASHCOUNT</b></dt>
<dt>0x2004</dt>
</dl>
</td>
<td width="60%">
Retrieves the number of times <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> will flash the taskbar button when rejecting a foreground switch request. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives the value.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETFOREGROUNDLOCKTIMEOUT"></a><a id="spi_getforegroundlocktimeout"></a><dl>
<dt><b>SPI_GETFOREGROUNDLOCKTIMEOUT</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Retrieves the amount of time following user input, in milliseconds, during which the system will not allow applications to force themselves into the foreground. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives the time.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMINIMIZEDMETRICS"></a><a id="spi_getminimizedmetrics"></a><dl>
<dt><b>SPI_GETMINIMIZEDMETRICS</b></dt>
<dt>0x002B</dt>
</dl>
</td>
<td width="60%">
Retrieves the metrics associated with minimized windows. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-minimizedmetrics">MINIMIZEDMETRICS</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(MINIMIZEDMETRICS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSEDOCKTHRESHOLD"></a><a id="spi_getmousedockthreshold"></a><dl>
<dt><b>SPI_GETMOUSEDOCKTHRESHOLD</b></dt>
<dt>0x007E</dt>
</dl>
</td>
<td width="60%">
Retrieves the threshold in pixels where docking behavior is triggered by using a mouse to drag a window to the edge of a monitor or monitor array. The default threshold is 1. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that receives the value.

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSEDRAGOUTTHRESHOLD"></a><a id="spi_getmousedragoutthreshold"></a><dl>
<dt><b>SPI_GETMOUSEDRAGOUTTHRESHOLD</b></dt>
<dt>0x0084</dt>
</dl>
</td>
<td width="60%">
Retrieves the threshold in pixels where undocking behavior is triggered by using a mouse to drag a window from the edge of a monitor or a monitor array toward the center. The default threshold is 20.

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETMOUSESIDEMOVETHRESHOLD"></a><a id="spi_getmousesidemovethreshold"></a><dl>
<dt><b>SPI_GETMOUSESIDEMOVETHRESHOLD</b></dt>
<dt>0x0088</dt>
</dl>
</td>
<td width="60%">
Retrieves the threshold in pixels from the top of a monitor or a monitor array where a vertically maximized window  is restored when dragged with the mouse. The default threshold is 50.

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETNONCLIENTMETRICS"></a><a id="spi_getnonclientmetrics"></a><dl>
<dt><b>SPI_GETNONCLIENTMETRICS</b></dt>
<dt>0x0029</dt>
</dl>
</td>
<td width="60%">
Retrieves the metrics associated with the nonclient area of nonminimized windows. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-nonclientmetricsa">NONCLIENTMETRICS</a> structure that receives the information. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(NONCLIENTMETRICS)</code>.

<b>Windows Server 2003 and Windows XP/2000:  </b>See Remarks for <a href="/windows/desktop/api/winuser/ns-winuser-nonclientmetricsa#remarks">NONCLIENTMETRICS</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETPENDOCKTHRESHOLD"></a><a id="spi_getpendockthreshold"></a><dl>
<dt><b>SPI_GETPENDOCKTHRESHOLD</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
<b>Retrieves the threshold in pixels where docking behavior is triggered by using a pen to drag a window to the edge of a monitor or monitor array. The default is 30.</b>

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETPENDRAGOUTTHRESHOLD"></a><a id="spi_getpendragoutthreshold"></a><dl>
<dt><b>SPI_GETPENDRAGOUTTHRESHOLD</b></dt>
<dt>0x0086</dt>
</dl>
</td>
<td width="60%">
Retrieves the threshold in pixels where undocking behavior is triggered by using a pen to drag a window from the edge of a monitor or monitor array toward its center. The default threshold is 30.

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETPENSIDEMOVETHRESHOLD"></a><a id="spi_getpensidemovethreshold"></a><dl>
<dt><b>SPI_GETPENSIDEMOVETHRESHOLD</b></dt>
<dt>0x008A</dt>
</dl>
</td>
<td width="60%">
Retrieves the threshold in pixels from the top of a monitor or monitor array where a vertically maximized window  is restored when dragged with the mouse. The default threshold is 50.

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSHOWIMEUI"></a><a id="spi_getshowimeui"></a><dl>
<dt><b>SPI_GETSHOWIMEUI</b></dt>
<dt>0x006E</dt>
</dl>
</td>
<td width="60%">
Determines whether the IME status window is visible (on a per-user basis). The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if the status window is visible, or <b>FALSE</b> if it is not.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETSNAPSIZING"></a><a id="spi_getsnapsizing"></a><dl>
<dt><b>SPI_GETSNAPSIZING</b></dt>
<dt>0x008E</dt>
</dl>
</td>
<td width="60%">
Determines whether a window is vertically maximized when it is sized to the top or bottom of a monitor or monitor array. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> otherwise.

Use <b>SPI_GETWINARRANGING</b> to determine whether this behavior is enabled.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_GETWINARRANGING"></a><a id="spi_getwinarranging"></a><dl>
<dt><b>SPI_GETWINARRANGING</b></dt>
<dt>0x0082</dt>
</dl>
</td>
<td width="60%">
Determines whether window arrangement is enabled. The <i>pvParam</i> parameter must point to a <b>BOOL</b> variable that receives <b>TRUE</b> if enabled, or <b>FALSE</b> otherwise.

Window arrangement reduces the number of mouse, pen, or touch interactions needed to move and size top-level windows by simplifying the default behavior of a window when it is dragged or sized.

The following parameters retrieve individual window arrangement settings:

<dl>
<dd><b>SPI_GETDOCKMOVING</b></dd>
<dd><b>SPI_GETMOUSEDOCKTHRESHOLD</b></dd>
<dd><b>SPI_GETMOUSEDRAGOUTTHRESHOLD</b></dd>
<dd><b>SPI_GETMOUSESIDEMOVETHRESHOLD</b></dd>
<dd><b>SPI_GETPENDOCKTHRESHOLD</b></dd>
<dd><b>SPI_GETPENDRAGOUTTHRESHOLD</b></dd>
<dd><b>SPI_GETPENSIDEMOVETHRESHOLD</b></dd>
<dd><b>SPI_GETSNAPSIZING</b></dd>
</dl>
<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETACTIVEWINDOWTRACKING"></a><a id="spi_setactivewindowtracking"></a><dl>
<dt><b>SPI_SETACTIVEWINDOWTRACKING</b></dt>
<dt>0x1001</dt>
</dl>
</td>
<td width="60%">
Sets active window tracking (activating the window the mouse is on) either on or off. Set <i>pvParam</i> to <b>TRUE</b> for on or <b>FALSE</b> for off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETACTIVEWNDTRKZORDER"></a><a id="spi_setactivewndtrkzorder"></a><dl>
<dt><b>SPI_SETACTIVEWNDTRKZORDER</b></dt>
<dt>0x100D</dt>
</dl>
</td>
<td width="60%">
Determines whether or not windows activated through active window tracking should be brought to the top. Set <i>pvParam</i> to <b>TRUE</b> for on or <b>FALSE</b> for off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETACTIVEWNDTRKTIMEOUT"></a><a id="spi_setactivewndtrktimeout"></a><dl>
<dt><b>SPI_SETACTIVEWNDTRKTIMEOUT</b></dt>
<dt>0x2003</dt>
</dl>
</td>
<td width="60%">
Sets the active window tracking delay. Set <i>pvParam</i> to the number of milliseconds to delay before activating the window under the mouse pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETANIMATION"></a><a id="spi_setanimation"></a><dl>
<dt><b>SPI_SETANIMATION</b></dt>
<dt>0x0049</dt>
</dl>
</td>
<td width="60%">
Sets the animation effects associated with user actions. The <i>pvParam</i> parameter must point to an <a href="/windows/desktop/api/winuser/ns-winuser-animationinfo">ANIMATIONINFO</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(ANIMATIONINFO)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETBORDER"></a><a id="spi_setborder"></a><dl>
<dt><b>SPI_SETBORDER</b></dt>
<dt>0x0006</dt>
</dl>
</td>
<td width="60%">
Sets the border multiplier factor that determines the width of a window's sizing border. The <i>uiParam</i> parameter specifies the new value.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETCARETWIDTH"></a><a id="spi_setcaretwidth"></a><dl>
<dt><b>SPI_SETCARETWIDTH</b></dt>
<dt>0x2007</dt>
</dl>
</td>
<td width="60%">
Sets the caret width in edit controls. Set <i>pvParam</i> to the desired width, in pixels. The default and minimum value is 1.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDOCKMOVING"></a><a id="spi_setdockmoving"></a><dl>
<dt><b>SPI_SETDOCKMOVING</b></dt>
<dt>0x0091</dt>
</dl>
</td>
<td width="60%">
Sets whether a window is docked when it is moved to the top, left, or right docking targets on a monitor or monitor array. Set <i>pvParam</i> to <b>TRUE</b> for on or <b>FALSE</b> for off.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDRAGFROMMAXIMIZE"></a><a id="spi_setdragfrommaximize"></a><dl>
<dt><b>SPI_SETDRAGFROMMAXIMIZE</b></dt>
<dt>0x008D</dt>
</dl>
</td>
<td width="60%">
Sets whether a maximized window is restored when its caption bar is dragged. Set <i>pvParam</i> to <b>TRUE</b> for on or <b>FALSE</b> for off.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDRAGFULLWINDOWS"></a><a id="spi_setdragfullwindows"></a><dl>
<dt><b>SPI_SETDRAGFULLWINDOWS</b></dt>
<dt>0x0025</dt>
</dl>
</td>
<td width="60%">
Sets dragging of full windows either on or off. The <i>uiParam</i> parameter specifies <b>TRUE</b> for on, or <b>FALSE</b> for off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDRAGHEIGHT"></a><a id="spi_setdragheight"></a><dl>
<dt><b>SPI_SETDRAGHEIGHT</b></dt>
<dt>0x004D</dt>
</dl>
</td>
<td width="60%">
Sets the height, in pixels, of the rectangle used to detect the start of a drag operation. Set <i>uiParam</i> to the new value. To retrieve the drag height, call <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with the <b>SM_CYDRAG</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETDRAGWIDTH"></a><a id="spi_setdragwidth"></a><dl>
<dt><b>SPI_SETDRAGWIDTH</b></dt>
<dt>0x004C</dt>
</dl>
</td>
<td width="60%">
Sets the width, in pixels, of the rectangle used to detect the start of a drag operation. Set <i>uiParam</i> to the new value. To retrieve the drag width, call <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with the <b>SM_CXDRAG</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFOREGROUNDFLASHCOUNT"></a><a id="spi_setforegroundflashcount"></a><dl>
<dt><b>SPI_SETFOREGROUNDFLASHCOUNT</b></dt>
<dt>0x2005</dt>
</dl>
</td>
<td width="60%">
Sets the number of times <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> will flash the taskbar button when rejecting a foreground switch request. Set <i>pvParam</i> to the number of times to flash.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETFOREGROUNDLOCKTIMEOUT"></a><a id="spi_setforegroundlocktimeout"></a><dl>
<dt><b>SPI_SETFOREGROUNDLOCKTIMEOUT</b></dt>
<dt>0x2001</dt>
</dl>
</td>
<td width="60%">
Sets the amount of time following user input, in milliseconds, during which the system does not allow applications to force themselves into the foreground. Set <i>pvParam</i> to the new time-out value.

The calling thread must be able to change the foreground window, otherwise the call fails.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMINIMIZEDMETRICS"></a><a id="spi_setminimizedmetrics"></a><dl>
<dt><b>SPI_SETMINIMIZEDMETRICS</b></dt>
<dt>0x002C</dt>
</dl>
</td>
<td width="60%">
Sets the metrics associated with minimized windows. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-minimizedmetrics">MINIMIZEDMETRICS</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(MINIMIZEDMETRICS)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEDOCKTHRESHOLD"></a><a id="spi_setmousedockthreshold"></a><dl>
<dt><b>SPI_SETMOUSEDOCKTHRESHOLD</b></dt>
<dt>0x007F</dt>
</dl>
</td>
<td width="60%">
Sets the threshold in pixels where docking behavior is triggered by using a mouse to drag a window to the edge of a monitor or monitor array. The default threshold is 1. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that contains the new value.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSEDRAGOUTTHRESHOLD"></a><a id="spi_setmousedragoutthreshold"></a><dl>
<dt><b>SPI_SETMOUSEDRAGOUTTHRESHOLD</b></dt>
<dt>0x0085</dt>
</dl>
</td>
<td width="60%">
Sets the threshold in pixels where undocking behavior is triggered by using a mouse to drag a window from the edge of a monitor or monitor array to its center. The default threshold is 20. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that contains the new value.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETMOUSESIDEMOVETHRESHOLD"></a><a id="spi_setmousesidemovethreshold"></a><dl>
<dt><b>SPI_SETMOUSESIDEMOVETHRESHOLD</b></dt>
<dt>0x0089</dt>
</dl>
</td>
<td width="60%">
Sets the threshold in pixels from the top of the monitor where a vertically maximized window is restored when dragged with the mouse. The default threshold is 50. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that contains the new value.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETNONCLIENTMETRICS"></a><a id="spi_setnonclientmetrics"></a><dl>
<dt><b>SPI_SETNONCLIENTMETRICS</b></dt>
<dt>0x002A</dt>
</dl>
</td>
<td width="60%">
Sets the metrics associated with the nonclient area of nonminimized windows. The <i>pvParam</i> parameter must point to a <a href="/windows/desktop/api/winuser/ns-winuser-nonclientmetricsa">NONCLIENTMETRICS</a> structure that contains the new parameters. Set the <b>cbSize</b> member of this structure and the <i>uiParam</i> parameter to <code>sizeof(NONCLIENTMETRICS)</code>. Also, the <b>lfHeight</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure must be a negative value.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETPENDOCKTHRESHOLD"></a><a id="spi_setpendockthreshold"></a><dl>
<dt><b>SPI_SETPENDOCKTHRESHOLD</b></dt>
<dt>0x0081</dt>
</dl>
</td>
<td width="60%">
Sets the threshold in pixels where docking behavior is triggered by using a pen to drag a window to the edge of a monitor or monitor array. The default threshold is 30. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that contains the new value.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETPENDRAGOUTTHRESHOLD"></a><a id="spi_setpendragoutthreshold"></a><dl>
<dt><b>SPI_SETPENDRAGOUTTHRESHOLD</b></dt>
<dt>0x0087</dt>
</dl>
</td>
<td width="60%">
Sets the threshold in pixels where undocking behavior is triggered by using a pen to drag a window from the edge of a monitor or monitor array to its center. The default threshold is 30. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that contains the new value.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETPENSIDEMOVETHRESHOLD"></a><a id="spi_setpensidemovethreshold"></a><dl>
<dt><b>SPI_SETPENSIDEMOVETHRESHOLD</b></dt>
<dt>0x008B</dt>
</dl>
</td>
<td width="60%">
Sets the threshold in pixels from the top of the monitor where a vertically maximized window is restored when dragged with a pen. The default threshold is 50. The <i>pvParam</i> parameter must point to a <b>DWORD</b> variable that contains the new value.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSHOWIMEUI"></a><a id="spi_setshowimeui"></a><dl>
<dt><b>SPI_SETSHOWIMEUI</b></dt>
<dt>0x006F</dt>
</dl>
</td>
<td width="60%">
Sets whether the IME status window is visible or not on a per-user basis. The <i>uiParam</i> parameter specifies <b>TRUE</b> for on or <b>FALSE</b> for off.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETSNAPSIZING"></a><a id="spi_setsnapsizing"></a><dl>
<dt><b>SPI_SETSNAPSIZING</b></dt>
<dt>0x008F</dt>
</dl>
</td>
<td width="60%">
Sets whether a window is vertically maximized when it is sized to the top or bottom of the monitor. Set <i>pvParam</i> to <b>TRUE</b> for on or <b>FALSE</b> for off.

<b>SPI_GETWINARRANGING</b> must be <b>TRUE</b> to enable this behavior.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SPI_SETWINARRANGING"></a><a id="spi_setwinarranging"></a><dl>
<dt><b>SPI_SETWINARRANGING</b></dt>
<dt>0x0083</dt>
</dl>
</td>
<td width="60%">
Sets whether window arrangement is enabled. Set <i>pvParam</i> to <b>TRUE</b> for on or <b>FALSE</b> for off.

Window arrangement reduces the number of mouse, pen, or touch interactions needed to move and size top-level windows by simplifying the default behavior of a window when it is dragged or sized.

The following parameters set individual window arrangement settings:

<dl>
<dd><b>SPI_SETDOCKMOVING</b></dd>
<dd><b>SPI_SETMOUSEDOCKTHRESHOLD</b></dd>
<dd><b>SPI_SETMOUSEDRAGOUTTHRESHOLD</b></dd>
<dd><b>SPI_SETMOUSESIDEMOVETHRESHOLD</b></dd>
<dd><b>SPI_SETPENDOCKTHRESHOLD</b></dd>
<dd><b>SPI_SETPENDRAGOUTTHRESHOLD</b></dd>
<dd><b>SPI_SETPENSIDEMOVETHRESHOLD</b></dd>
<dd><b>SPI_SETSNAPSIZING</b></dd>
</dl>
<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This parameter is not supported.

</td>
</tr>
</table>

### -param uiParam [in]

Type: <b>UINT</b>

A parameter whose usage and format depends on the system parameter being queried or set. For more information about system-wide parameters, see the <i>uiAction</i> parameter. If not otherwise indicated, you must specify zero for this parameter.

### -param pvParam [in, out]

Type: <b>PVOID</b>

A parameter whose usage and format depends on the system parameter being queried or set. For more information about system-wide parameters, see the <i>uiAction</i> parameter. If not otherwise indicated, you must specify <b>NULL</b> for this parameter. For information on the <b>PVOID</b> datatype, see <a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>.

### -param fWinIni [in]

Type: <b>UINT</b>

If a system parameter is being set, specifies whether the user profile is to be updated, and if so, whether the <a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a> message is to be broadcast to all top-level windows to notify them of the change.

This parameter can be zero if you do not want to update the user profile or broadcast the <a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a> message, or it can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPIF_UPDATEINIFILE"></a><a id="spif_updateinifile"></a><dl>
<dt><b>SPIF_UPDATEINIFILE</b></dt>
</dl>
</td>
<td width="60%">
Writes the new system-wide parameter setting to the user profile.

</td>
</tr>
<tr>
<td width="40%"><a id="SPIF_SENDCHANGE"></a><a id="spif_sendchange"></a><dl>
<dt><b>SPIF_SENDCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Broadcasts the <a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a> message after updating the user profile.

</td>
</tr>
<tr>
<td width="40%"><a id="SPIF_SENDWININICHANGE"></a><a id="spif_sendwininichange"></a><dl>
<dt><b>SPIF_SENDWININICHANGE</b></dt>
</dl>
</td>
<td width="60%">
Same as <b>SPIF_SENDCHANGE</b>.

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is intended for use with applications that allow the user to customize the environment.

A keyboard layout name should be derived from the hexadecimal value of the language identifier corresponding to the layout. For example, U.S. English has a language identifier of 0x0409, so the primary U.S. English layout is named "00000409". Variants of U.S. English layout, such as the Dvorak layout, are named "00010409", "00020409" and so on. For a list of the primary language identifiers and sublanguage identifiers that make up a language identifier, see the <b>MAKELANGID</b> macro.

There is a difference between the High Contrast color scheme and the High Contrast Mode. The High Contrast color scheme changes the system colors to colors that have obvious contrast; you switch to this color scheme by using the Display Options in the control panel. The High Contrast Mode, which uses <b>SPI_GETHIGHCONTRAST</b> and <b>SPI_SETHIGHCONTRAST</b>, advises applications to modify their appearance for visually-impaired users. It involves such things as audible warning to users and customized color scheme (using the Accessibility Options in the control panel). For more information, see <a href="/windows/desktop/api/winuser/ns-winuser-highcontrasta">HIGHCONTRAST</a>. For more information on general accessibility features, see <a href="/windows/desktop/accessibility">Accessibility</a>.

During the time that the primary button is held down to activate the Mouse ClickLock feature, the user can move the mouse. After the primary button is locked down, releasing the primary button does not result in a <b>WM_LBUTTONUP</b> message. Thus, it will appear to an application that the primary button is still down. Any subsequent button message releases the primary button, sending a <b>WM_LBUTTONUP</b> message to the application, thus the button can be unlocked programmatically or through the user clicking any button.

This API is not DPI aware, and should not be used if the calling thread is per-monitor DPI aware. For the DPI-aware version of this API, see <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfofordpi">SystemParametersInfoForDPI</a>. For more information on DPI awareness, see <a href="/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows">the Windows High DPI documentation.</a>



#### Examples

The following example uses <b>SystemParametersInfo</b> to double the mouse speed.


```cpp

#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "user32.lib")    

void main()  
{     
    BOOL fResult;
    int aMouseInfo[3];    // Array for mouse information
    
    // Get the current mouse speed.         
    fResult = SystemParametersInfo(SPI_GETMOUSE,   // Get mouse information
                                   0,              // Not used
                                   &aMouseInfo,    // Holds mouse information
                                   0);             // Not used           
                                   
    // Double it.         
    if( fResult )     
    {
        aMouseInfo[2] = 2 * aMouseInfo[2];
        
        // Change the mouse speed to the new value.
        SystemParametersInfo(SPI_SETMOUSE,      // Set mouse information
                             0,                 // Not used
                             aMouseInfo,        // Mouse information
                             SPIF_SENDCHANGE);  // Update Win.ini
    }  
}
```






> [!NOTE]
> The winuser.h header defines SystemParametersInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/ns-winuser-accesstimeout">ACCESSTIMEOUT</a>



<a href="/windows/desktop/api/winuser/ns-winuser-animationinfo">ANIMATIONINFO</a>



<a href="/windows/desktop/api/winuser/ns-winuser-audiodescription">AUDIODESCRIPTION</a>



<a href="/windows/desktop/api/winuser/ns-winuser-filterkeys">FILTERKEYS</a>



<a href="/windows/desktop/api/winuser/ns-winuser-highcontrasta">HIGHCONTRAST</a>



<a href="/windows/desktop/api/winuser/ns-winuser-iconmetricsa">ICONMETRICS</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>



<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<a href="/windows/desktop/api/winuser/ns-winuser-minimizedmetrics">MINIMIZEDMETRICS</a>



<a href="/windows/desktop/api/winuser/ns-winuser-mousekeys">MOUSEKEYS</a>



<a href="/windows/desktop/api/winuser/ns-winuser-nonclientmetricsa">NONCLIENTMETRICS</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/ns-winuser-serialkeysa">SERIALKEYS</a>



<a href="/windows/desktop/api/winuser/ns-winuser-soundsentrya">SOUNDSENTRY</a>



<a href="/windows/desktop/api/winuser/ns-winuser-stickykeys">STICKYKEYS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfofordpi">SystemParametersInfoForDPI</a>



<a href="/windows/desktop/api/winuser/ns-winuser-togglekeys">TOGGLEKEYS</a>



<a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a>



<a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>
