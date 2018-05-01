---
UID: NS:shellapi._NOTIFYICONDATAA
title: "_NOTIFYICONDATAA"
author: windows-driver-content
description: Contains information that the system needs to display notifications in the notification area. Used by Shell_NotifyIcon.
old-location: shell\NOTIFYICONDATA.htm
old-project: shell
ms.assetid: fdcc42c1-b3e5-4b04-8d79-7b6c29699d53
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: "*PNOTIFYICONDATAA, 0, NIF_GUID, NIF_ICON, NIF_INFO, NIF_MESSAGE, NIF_REALTIME, NIF_SHOWTIP, NIF_STATE, NIF_TIP, NIIF_ERROR, NIIF_ICON_MASK, NIIF_INFO, NIIF_LARGE_ICON, NIIF_NONE, NIIF_NOSOUND, NIIF_RESPECT_QUIET_TIME, NIIF_USER, NIIF_WARNING, NIS_HIDDEN, NIS_SHAREDICON, NOTIFYICONDATA, NOTIFYICONDATA structure [Windows Shell], NOTIFYICONDATAA, NOTIFYICON_VERSION, NOTIFYICON_VERSION_4, PNOTIFYICONDATA, PNOTIFYICONDATA structure pointer [Windows Shell], _NOTIFYICONDATAA, _win32_NOTIFYICONDATA, shell.NOTIFYICONDATA, shellapi/NOTIFYICONDATA, shellapi/PNOTIFYICONDATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NOTIFYICONDATAA, *PNOTIFYICONDATAA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Shellapi.h
api_name:
-	NOTIFYICONDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _NOTIFYICONDATAA structure


## -description


Contains information that the system needs to display notifications in the notification area. Used by <a href="https://msdn.microsoft.com/a316bc29-5f19-4a04-a32b-f4caeea0c029">Shell_NotifyIcon</a>.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.


### -field hWnd

Type: <b>HWND</b>

A handle to the window that receives notifications associated with an icon in the notification area.


### -field uID

Type: <b>UINT</b>

The application-defined identifier of the taskbar icon. The Shell uses either (<b>hWnd</b> plus <b>uID</b>) or <b>guidItem</b> to identify which icon to operate on when <a href="https://msdn.microsoft.com/a316bc29-5f19-4a04-a32b-f4caeea0c029">Shell_NotifyIcon</a> is invoked. You can have multiple icons associated with a single <b>hWnd</b> by assigning each a different <b>uID</b>. If <b>guidItem</b> is specified, <b>uID</b> is ignored.


### -field uFlags

Type: <b>UINT</b>

Flags that either indicate which of the other members of the structure contain valid data or provide additional information to the tooltip as to how it should display. This member can be a combination of the following values:



#### NIF_MESSAGE (0x00000001)

0x00000001. The <b>uCallbackMessage</b> member is valid.



#### NIF_ICON (0x00000002)

0x00000002. The <b>hIcon</b> member is valid.



#### NIF_TIP (0x00000004)

0x00000004. The <b>szTip</b> member is valid.



#### NIF_STATE (0x00000008)

0x00000008. The <b>dwState</b> and <b>dwStateMask</b> members are valid.



#### NIF_INFO (0x00000010)

0x00000010. Display a balloon notification. The <b>szInfo</b>, <b>szInfoTitle</b>, <b>dwInfoFlags</b>, and <b>uTimeout</b> members are valid. Note that <b>uTimeout</b> is valid only in Windows 2000 and Windows XP.
        
                                

<ul>
<li>To display the balloon notification, specify NIF_INFO and provide text in <b>szInfo</b>.</li>
<li>To remove a balloon notification, specify NIF_INFO and provide an empty string through <b>szInfo</b>.</li>
<li>To add a notification area icon without displaying a notification, do not set the NIF_INFO flag.</li>
</ul>


#### NIF_GUID (0x00000020)

0x00000020. 
                                

<ul>
<li><b>Windows 7 and later</b>: The <b>guidItem</b> is valid.</li>
<li><b>Windows Vista and earlier</b>: Reserved.</li>
</ul>


#### NIF_REALTIME (0x00000040)

0x00000040. <b>Windows Vista and later</b>. If the balloon notification cannot be displayed immediately, discard it. Use this flag for notifications that represent real-time information which would be meaningless or misleading if displayed at a later time. For example, a message that states "Your telephone is ringing." NIF_REALTIME is meaningful only when combined with the NIF_INFO flag.



#### NIF_SHOWTIP (0x00000080)

0x00000080. <b>Windows Vista and later</b>. Use the standard tooltip. Normally, when <b>uVersion</b> is set to NOTIFYICON_VERSION_4, the standard tooltip is suppressed and can be replaced by the application-drawn, pop-up UI. If the application wants to show the standard tooltip with NOTIFYICON_VERSION_4, it can specify NIF_SHOWTIP to indicate the standard tooltip should still be shown.


### -field uCallbackMessage

Type: <b>UINT</b>

An application-defined message identifier. The system uses this identifier to send notification messages to the window identified in <b>hWnd</b>. These notification messages are sent when a mouse event or hover occurs in the bounding rectangle of the icon, when the icon is selected or activated with the keyboard, or when those actions occur in the balloon notification.



When the <b>uVersion</b> member is either 0 or NOTIFYICON_VERSION, the <i>wParam</i> parameter of the message contains the identifier of the taskbar icon in which the event occurred. This identifier can be 32 bits in length. The <i>lParam</i> parameter holds the mouse or keyboard message associated with the event. For example, when the pointer moves over a taskbar icon, <i>lParam</i> is set to <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a>.

When the <b>uVersion</b> member is NOTIFYICON_VERSION_4, applications continue to receive notification events in the form of application-defined messages through the <b>uCallbackMessage</b> member, but the interpretation of the <i>lParam</i> and <i>wParam</i> parameters of that message is changed as follows:

<ul>
<li>
<a href="https://msdn.microsoft.com/4f169f33-ed13-4efc-bf3f-ea2a4fe1de4e">LOWORD(lParam)</a> contains notification events, such as NIN_BALLOONSHOW, NIN_POPUPOPEN, or WM_CONTEXTMENU.</li>
<li>
<a href="https://msdn.microsoft.com/9f79d489-ff3f-437c-821e-fd353d712c7b">HIWORD(lParam)</a> contains the icon ID. Icon IDs are restricted to a length of 16 bits.</li>
<li>
<a href="https://msdn.microsoft.com/40f7dde6-1486-4050-b9b6-ffc2ed9982a9">GET_X_LPARAM(wParam)</a> returns the X anchor coordinate for notification events NIN_POPUPOPEN, NIN_SELECT, NIN_KEYSELECT, and all mouse messages between WM_MOUSEFIRST and WM_MOUSELAST. If any of those messages are generated by the keyboard, <i>wParam</i> is set to the upper-left corner of the target icon. For all other messages, <i>wParam</i> is undefined.</li>
<li>
<a href="https://msdn.microsoft.com/eaf1b26d-14e7-45e9-bdd1-79258c5f9701">GET_Y_LPARAM(wParam)</a> returns the Y anchor coordinate for notification events and messages as defined for the X anchor.</li>
</ul>

### -field hIcon

Type: <b>HICON</b>

A handle to the icon to be added, modified, or deleted. Windows XP and later support icons of up to 32 BPP.

If only a 16x16 pixel icon is provided, it is scaled to a larger size in a system set to a high dpi value. This can lead to an unattractive result. It is recommended that you provide both a 16x16 pixel icon and a 32x32 icon in your resource file. Use <a href="https://msdn.microsoft.com/8dee876d-1c94-47ef-b28d-effc80dab14e">LoadIconMetric</a> to ensure that the correct icon is loaded and scaled appropriately. See Remarks for a code example.


### -field szTip

Type: <b>TCHAR[64]</b>

A null-terminated string that specifies the text for a standard tooltip. It can have a maximum of 64 characters, including the terminating null character.



For Windows 2000 and later, <b>szTip</b> can have a maximum of 128 characters, including the terminating null character.


### -field dwState

Type: <b>DWORD</b>

<b>Windows 2000 and later</b>. The state of the icon. One or both of the following values:



#### NIS_HIDDEN (0x00000001)

0x00000001. The icon is hidden.



#### NIS_SHAREDICON (0x00000002)

0x00000002. The icon resource is shared between multiple icons.


### -field dwStateMask

Type: <b>DWORD</b>

<b>Windows 2000 and later</b>. A value that specifies which bits of the <b>dwState</b> member are retrieved or modified. The possible values are the same as those for <b>dwState</b>. For example, setting this member to <b>NIS_HIDDEN</b> causes only the item's hidden state to be modified while the icon sharing bit is ignored regardless of its value.


### -field szInfo

Type: <b>TCHAR[256]</b>

<b>Windows 2000 and later</b>. A null-terminated string that specifies the text to display in a balloon notification. It can have a maximum of 256 characters, including the terminating null character, but should be restricted to 200 characters in English to accommodate localization. To remove the balloon notification from the UI, either delete the icon (with <a href="https://msdn.microsoft.com/a316bc29-5f19-4a04-a32b-f4caeea0c029">NIM_DELETE</a>) or set the <b>NIF_INFO</b> flag in <b>uFlags</b> and set <b>szInfo</b> to an empty string.


### -field DUMMYUNIONNAME

 


### -field szInfoTitle

Type: <b>TCHAR[64]</b>

<b>Windows 2000 and later</b>. A null-terminated string that specifies a title for a balloon notification. This title appears in a larger font immediately above the text. It can have a maximum of 64 characters, including the terminating null character, but should be restricted to 48 characters in English to accommodate localization.


### -field dwInfoFlags

Type: <b>DWORD</b>

<b>Windows 2000 and later</b>. Flags that can be set to modify the behavior and appearance of a balloon notification. The icon is placed to the left of the title. If the <b>szInfoTitle</b> member is zero-length, the icon is not shown.



#### NIIF_NONE (0x00000000)

0x00000000. No icon.



#### NIIF_INFO (0x00000001)

0x00000001. An information icon.



#### NIIF_WARNING (0x00000002)

0x00000002. A warning icon.



#### NIIF_ERROR (0x00000003)

0x00000003. An error icon.



#### NIIF_USER (0x00000004)

0x00000004. <b>Windows XP SP2 and later</b>. 
        
                                

<ul>
<li><b>Windows XP</b>: Use the icon identified in <b>hIcon</b> as the notification balloon's title icon.</li>
<li><b>Windows Vista and later</b>: Use the icon identified in <b>hBalloonIcon</b> as the notification balloon's title icon.</li>
</ul>


#### NIIF_NOSOUND (0x00000010)

0x00000010. <b>Windows XP and later</b>. Do not play the associated sound. Applies only to notifications.



#### NIIF_LARGE_ICON (0x00000020)

0x00000020. <b>Windows Vista and later</b>. The large version of the icon should be used as the notification icon. This corresponds to the icon with dimensions SM_CXICON x SM_CYICON. If this flag is not set, the icon with dimensions XM_CXSMICON x SM_CYSMICON is used. 
        
                                

<ul>
<li>This flag can be used with all <a href="https://msdn.microsoft.com/37da5555-3626-465e-b834-3a28b75495c4">stock icons</a>.</li>
<li>Applications that use older customized icons (NIIF_USER with <b>hIcon</b>) must provide a new SM_CXICON x SM_CYICON version in the tray icon (<b>hIcon</b>). These icons are scaled down when they are displayed in the System Tray or System Control Area (SCA).</li>
<li>New customized icons (NIIF_USER with <b>hBalloonIcon</b>) must supply an SM_CXICON x SM_CYICON version in the supplied icon (<b>hBalloonIcon</b>).</li>
</ul>


#### NIIF_RESPECT_QUIET_TIME (0x00000080)

0x00000080. <b>Windows 7 and later</b>. Do not display the balloon notification if the current user is in "quiet time", which is the first hour after a new user logs into his or her account for the first time. During this time, most notifications should not be sent or shown. This lets a user become accustomed to a new computer system without those distractions. Quiet time also occurs for each user after an operating system upgrade or clean installation. A notification sent with this flag during quiet time is not queued; it is simply dismissed unshown. The application can resend the notification later if it is still valid at that time.

Because an application cannot predict when it might encounter quiet time, we recommended that this flag always be set on all appropriate notifications by any application that means to honor quiet time.

During quiet time, certain notifications should still be sent because they are expected by the user as feedback in response to a user action, for instance when he or she plugs in a USB device or prints a document.

If the current user is not in quiet time, this flag has no effect.



#### NIIF_ICON_MASK (0x0000000F)

0x0000000F. <b>Windows XP and later</b>. Reserved.


### -field guidItem

Type: <b>GUID</b>

<b>Windows XP and later</b>.
                    
                        

<ul>
<li><b>Windows 7 and later</b>: A registered GUID that identifies the icon. This value overrides <b>uID</b> and is the recommended method of identifying the icon. The NIF_GUID flag must be set in the <b>uFlags</b> member.</li>
<li><b>Windows XP and Windows Vista</b>: Reserved; must be set to 0.</li>
</ul>
If your application is intended to run on both Windows Vista and Windows 7, it is imperative that you check the version of Windows and only specify a nonzero <b>guidItem</b> if on Windows 7 or later.

If you identify the notification icon with a GUID in one call to <a href="https://msdn.microsoft.com/a316bc29-5f19-4a04-a32b-f4caeea0c029">Shell_NotifyIcon</a>, you must use that same GUID to identify the icon in any subsequent <b>Shell_NotifyIcon</b> calls that deal with that same icon.

To generate a GUID for use in this member, use a GUID-generating tool such as Guidgen.exe.


### -field hBalloonIcon

Type: <b>HICON</b>

<b>Windows Vista and later</b>. The handle of a customized notification icon provided by the application that should be used independently of the notification area icon. If this member is non-NULL and the NIIF_USER flag is set in the <b>dwInfoFlags</b> member, this icon is used as the notification icon. If this member is <b>NULL</b>, the legacy behavior is carried out.


#### - uTimeout

Type: <b>UINT</b>

<b>Windows 2000 and later</b>. 
    
                            

<div class="alert"><b>Note</b>  This member is deprecated as of Windows Vista. Notification display times are now based on system accessibility settings.</div>
<div> </div>
Union with <b>uVersion</b>. The timeout value, in milliseconds, for notification. The system enforces minimum and maximum timeout values. Values specified in <b>uTimeout</b> that are too large are set to the maximum value. Values that are too small default to the minimum value. The system minimum and maximum timeout values are currently set at 10 seconds and 30 seconds, respectively. See Remarks for further discussion of <b>uTimeout</b>.


#### - uVersion

Type: <b>UINT</b>

<b>Windows 2000 and later</b>. Union with <b>uTimeout</b> (deprecated as of Windows Vista). Specifies which version of the Shell notification icon interface should be used. For more information on the differences in these versions, see <a href="https://msdn.microsoft.com/a316bc29-5f19-4a04-a32b-f4caeea0c029">Shell_NotifyIcon</a>. This member is employed only when using <b>Shell_NotifyIcon</b> to send an <b>NIM_SETVERSION</b> message.



#### 0

Use this value for applications designed for Windows versions prior to Windows 2000.



#### NOTIFYICON_VERSION

Use the Windows 2000 behavior. Use this value for applications designed for Windows 2000 and later.



#### NOTIFYICON_VERSION_4

Use the current behavior. Use this value for applications designed for Windows Vista and later.


## -remarks



See <a href="http://go.microsoft.com/fwlink/p/?linkid=200328">Notifications</a> in the Windows User Experience Interaction Guidelines for more information on notification UI and content best practices.

If you set the <b>NIF_INFO</b> flag in the <b>uFlags</b> member, the balloon-style notification is used. For more discussion of these notifications, see <a href="https://msdn.microsoft.com/4486b406-a069-4250-b7ab-671d895b79f9">Balloon tooltips</a>.

No more than one balloon notification at a time can be displayed for the taskbar. If an application attempts to display a notification when one is already being displayed, the new notification is queued and displayed when the older notification goes away. In versions of Windows before Windows Vista, the new notification would not appear until the existing notification has been visible for at least the system minimum timeout length, regardless of the original notification's <b>uTimeout</b> value. If the user does not appear to be using the computer, the system does not count this time toward the timeout.

Several members of this structure are only supported for Windows 2000 and later. To enable these members, include one of the following lines in your header:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Windows Vista and later:
#define NTDDI_VERSION NTDDI_WIN2K
#define NTDDI_VERSION NTDDI_WINXP
#define NTDDI_VERSION NTDDI_VISTA

// Windows XP and earlier:
#define _WIN32_IE 0x0500
</pre>
</td>
</tr>
</table></span></div>
Note that you must initialize the structure with its size. If you use the size of the currently defined structure, the application might not run with earlier versions of Shell32.dll, which expect a smaller structure. You can run your application against earlier versions of Shell32.dll by defining the appropriate version number (see <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Shell and Common Controls Versions</a>). However, this might cause problems if your application also needs to run on more recent systems.

You can maintain application compatibility with all Shell32.dll versions while still using the current header files by setting the size of the <b>NOTIFYICONDATA</b> structure appropriately. Before you initialize the structure, use <a href="https://msdn.microsoft.com/d7ec0f7d-ba2f-4aa4-b867-a2615244a580">DllGetVersion</a> to determine which Shell32.dll version is installed on the system and initialize <b>cbSize</b> with one of these values:

<table class="clsStd">
<tr>
<th>Shell32.dll Version</th>
<th>cbSize</th>
</tr>
<tr>
<td>6.0.6 or higher (Windows Vista and later)</td>
<td>sizeof(NOTIFYICONDATA)</td>
</tr>
<tr>
<td>6.0 (Windows XP)</td>
<td>NOTIFYICONDATA_V3_SIZE</td>
</tr>
<tr>
<td>5.0 (Windows 2000)</td>
<td>NOTIFYICONDATA_V2_SIZE</td>
</tr>
<tr>
<td>Versions lower than 5.0</td>
<td>NOTIFYICONDATA_V1_SIZE</td>
</tr>
</table>
 

Using this value for <b>cbSize</b> allows your application to use <b>NOTIFYICONDATA</b> in a method compatible with earlier Shell32.dll versions.

The following code example shows version checking that can enable an application that uses the <b>guidItem</b> member to run on both Windows Vista and Windows 7. It provides a Boolean function that returns <b>TRUE</b> if the operating system is Windows 7. Unless this member returns <b>TRUE</b>, the <b>guidItem</b> member must be set to 0.

                

<div class="alert"><b>Note</b>  This code is specific to the Windows 7 version number. It is expected that future versions of Windows and Windows Server will support the <b>guidItem</b> member, and at that time this code must be updated to identify later version numbers as valid as well.</div>
<div> </div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL IsWin7OrLater()
{
    // Initialize the OSVERSIONINFOEX structure.
    OSVERSIONINFOEX osvi;
    ZeroMemory(&amp;osvi, sizeof(OSVERSIONINFOEX));
    osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
    osvi.dwMajorVersion = 6;
    osvi.dwMinorVersion = 1;

    // Initialize the condition mask.
    DWORDLONG dwlConditionMask = 0;
    VER_SET_CONDITION(dwlConditionMask, VER_MAJORVERSION, VER_GREATER_EQUAL);
    VER_SET_CONDITION(dwlConditionMask, VER_MINORVERSION, VER_GREATER_EQUAL);

    // Perform the test.
    return VerifyVersionInfo(&amp;osvi, 
                             VER_MAJORVERSION | VER_MINORVERSION,
                             dwlConditionMask);
}
</pre>
</td>
</tr>
</table></span></div>
The following code example shows the use of <a href="https://msdn.microsoft.com/8dee876d-1c94-47ef-b28d-effc80dab14e">LoadIconMetric</a> to load an icon for use with high DPI.
            
                

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Declare NOTIFYICONDATA details. 
// Error handling is omitted here for brevity. Do not omit it in your code.

NOTIFYICONDATA nid = {};
nid.cbSize = sizeof(nid);
nid.hWnd = hWnd;
nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;

// Note: This is an example GUID only and should not be used.
// Normally, you should use a GUID-generating tool to provide the value to
// assign to guidItem.
static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
nid.guidItem = myGUID;

// This text will be shown as the icon's tooltip.
StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");

// Load the icon for high DPI.
LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &amp;(nid.hIcon));

// Show the notification.
Shell_NotifyIcon(NIM_ADD, &amp;nid) ? S_OK : E_FAIL;
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Troubleshooting"></a><a id="troubleshooting"></a><a id="TROUBLESHOOTING"></a>Troubleshooting</h3>
If you are using the <b>guidItem</b> member to identify the icon, and that icon is not seen or some calls to <a href="https://msdn.microsoft.com/a316bc29-5f19-4a04-a32b-f4caeea0c029">Shell_NotifyIcon</a> fail, one of the following cases is the likely cause:
    
                    

<ol>
<li>The NIF_GUID flag was not set in every call to <a href="https://msdn.microsoft.com/a316bc29-5f19-4a04-a32b-f4caeea0c029">Shell_NotifyIcon</a>. Once you identify the notification icon with a GUID in one call to <b>Shell_NotifyIcon</b>, you must use that same GUID to identify the icon in any subsequent <b>Shell_NotifyIcon</b> calls that deal with that same icon.</li>
<li>
The binary file that contains the icon was moved. The path of the binary file is included in the registration of the icon's GUID and cannot be changed. Settings associated with the icon are preserved through an upgrade only if the file path and GUID are unchanged. If the path must be changed, the application should remove any GUID information that was added when the existing icon was registered. Once that information is removed, you can move the binary file to a new location and reregister it with a new GUID. Any settings associated with the original GUID registration will be lost.

This also occurs in the case of a side-by-side installation. When dealing with a side-by-side installation, new versions of the application should update the GUID of the binary file.

<div class="alert"><b>Note</b>  The only exception to a moved file occurs when both the original and moved binary files are <a href="_inet_Authenticode_node_entry">Authenticode</a>-signed by the same company. In that case, settings are preserved through the move.</div>
<div> </div>
</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/D37E2BF7-1887-4780-81AD-85B2117321E4">Notifications and the Notification Area</a>
 

 

