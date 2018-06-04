---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _browseinfoW structure


## -description


Contains parameters for the <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> function and receives information about the folder selected by the user.


## -struct-fields




### -field hwndOwner

Type: <b>HWND</b>

A handle to the owner window for the dialog box.


### -field pidlRoot

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that specifies the location of the root folder from which to start browsing. Only the specified folder and its subfolders in the namespace hierarchy appear in the dialog box. This member can be <b>NULL</b>; in that case, a default location is used.


### -field pszDisplayName

Type: <b>LPTSTR</b>

Pointer to a buffer to receive the display name of the folder selected by the user. The size of this buffer is assumed to be MAX_PATH characters.


### -field lpszTitle

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that is displayed above the tree view control in the dialog box. This string can be used to specify instructions to the user.


### -field ulFlags

Type: <b>UINT</b>

Flags that specify the options for the dialog box. This member can be 0 or a combination of the following values. Version numbers refer to the minimum version of Shell32.dll required for <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> to recognize flags added in later releases. See <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Shell and Common Controls Versions</a> for more information.





#### BIF_RETURNONLYFSDIRS (0x00000001)

0x00000001. Only return file system directories. If the user selects folders that are not part of the file system, the <b>OK</b> button is grayed.

                        

<div class="alert"><b>Note</b>  The <b>OK</b> button remains enabled for "\\server" items, as well as "\\server\share" and directory items. However, if the user selects a "\\server" item, passing the PIDL returned by <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> to <a href="https://msdn.microsoft.com/f043ffa2-37c1-465d-aed6-0475e721fbde">SHGetPathFromIDList</a> fails.</div>
<div> </div>


#### BIF_DONTGOBELOWDOMAIN (0x00000002)

0x00000002. Do not include network folders below the domain level in the dialog box's tree view control.



#### BIF_STATUSTEXT (0x00000004)

0x00000004. Include a status area in the dialog box. The callback function can set the status text by sending messages to the dialog box. This flag is not supported when BIF_NEWDIALOGSTYLE is specified.



#### BIF_RETURNFSANCESTORS (0x00000008)

0x00000008. Only return file system ancestors. An ancestor is a subfolder that is beneath the root folder in the namespace hierarchy. If the user selects an ancestor of the root folder that is not part of the file system, the <b>OK</b> button is grayed.



#### BIF_EDITBOX (0x00000010)

0x00000010. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.71</a>. Include an edit control in the browse dialog box that allows the user to type the name of an item.



#### BIF_VALIDATE (0x00000020)

0x00000020. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.71</a>. If the user types an invalid name into the edit box, the browse dialog box calls the application's <a href="https://msdn.microsoft.com/e9109f38-34c7-46c0-aa0c-a6b4570f1c3a">BrowseCallbackProc</a> with the <b>BFFM_VALIDATEFAILED</b> message. This flag is ignored if BIF_EDITBOX is not specified.



#### BIF_NEWDIALOGSTYLE (0x00000040)

0x00000040. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. Use the new user interface. Setting this flag provides the user with a larger dialog box that can be resized. The dialog box has several new capabilities, including: drag-and-drop capability within the dialog box, reordering, shortcut menus, new folders, delete, and other shortcut menu commands.

                        

<div class="alert"><b>Note</b>  If COM is initialized through <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> with the COINIT_MULTITHREADED flag set, <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> fails if BIF_NEWDIALOGSTYLE is passed.</div>
<div> </div>


#### BIF_BROWSEINCLUDEURLS (0x00000080)

0x00000080. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. The browse dialog box can display URLs. The BIF_USENEWUI and BIF_BROWSEINCLUDEFILES flags must also be set. If any of these three flags are not set, the browser dialog box rejects URLs. Even when these flags are set, the browse dialog box displays URLs only if the folder that contains the selected item supports URLs. When the folder's <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a> method is called to request the selected item's attributes, the folder must set the <b>SFGAO_FOLDER</b> attribute flag. Otherwise, the browse dialog box will not display the URL.



#### BIF_USENEWUI


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. Use the new user interface, including an edit box. This flag is equivalent to BIF_EDITBOX | BIF_NEWDIALOGSTYLE.

                        

<div class="alert"><b>Note</b>  If COM is initialized through <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> with the COINIT_MULTITHREADED flag set, <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> fails if BIF_USENEWUI is passed.</div>
<div> </div>


#### BIF_UAHINT (0x00000100)

0x00000100. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 6.0</a>. When combined with BIF_NEWDIALOGSTYLE, adds a usage hint to the dialog box, in place of the edit box. BIF_EDITBOX overrides this flag.



#### BIF_NONEWFOLDERBUTTON (0x00000200)

0x00000200. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 6.0</a>. Do not include the <b>New Folder</b> button in the browse dialog box.



#### BIF_NOTRANSLATETARGETS (0x00000400)

0x00000400. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 6.0</a>. When the selected item is a shortcut, return the PIDL of the shortcut itself rather than its target.



#### BIF_BROWSEFORCOMPUTER (0x00001000)

0x00001000. Only return computers. If the user selects anything other than a computer, the <b>OK</b> button is grayed.



#### BIF_BROWSEFORPRINTER (0x00002000)

0x00002000. Only allow the selection of printers. If the user selects anything other than a printer, the <b>OK</b> button is grayed. 
               
                        

In Windows XP and later systems, the best practice is to use a Windows XP-style dialog, setting the root of the dialog to the <b>Printers and Faxes</b> folder (CSIDL_PRINTERS).



#### BIF_BROWSEINCLUDEFILES (0x00004000)

0x00004000. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.71</a>. The browse dialog box displays files as well as folders.



#### BIF_SHAREABLE (0x00008000)

0x00008000. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. The browse dialog box can display sharable resources on remote systems. This is intended for applications that want to expose remote shares on a local system. The BIF_NEWDIALOGSTYLE flag must also be set.



#### BIF_BROWSEFILEJUNCTIONS (0x00010000)

0x00010000. <b>Windows 7 and later</b>. Allow folder junctions such as a library or a compressed file with a .zip file name extension to be browsed.


### -field lpfn

Type: <b>BFFCALLBACK</b>

Pointer to an application-defined function that the dialog box calls when an event occurs. For more information, see the <a href="https://msdn.microsoft.com/e9109f38-34c7-46c0-aa0c-a6b4570f1c3a">BrowseCallbackProc</a> function. This member can be <b>NULL</b>.


### -field lParam

Type: <b>LPARAM</b>

An application-defined value that the dialog box passes to the callback function, if one is specified in <b>lpfn</b>.


### -field iImage

Type: <b>int</b>

An integer value that receives the index of the image associated with the selected folder, stored in the system image list.


##### - ulFlags.BIF_BROWSEFILEJUNCTIONS (0x00010000)

0x00010000. <b>Windows 7 and later</b>. Allow folder junctions such as a library or a compressed file with a .zip file name extension to be browsed.


##### - ulFlags.BIF_BROWSEFORCOMPUTER (0x00001000)

0x00001000. Only return computers. If the user selects anything other than a computer, the <b>OK</b> button is grayed.


##### - ulFlags.BIF_BROWSEFORPRINTER (0x00002000)

0x00002000. Only allow the selection of printers. If the user selects anything other than a printer, the <b>OK</b> button is grayed. 
               
                        

In Windows XP and later systems, the best practice is to use a Windows XP-style dialog, setting the root of the dialog to the <b>Printers and Faxes</b> folder (CSIDL_PRINTERS).


##### - ulFlags.BIF_BROWSEINCLUDEFILES (0x00004000)

0x00004000. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.71</a>. The browse dialog box displays files as well as folders.


##### - ulFlags.BIF_BROWSEINCLUDEURLS (0x00000080)

0x00000080. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. The browse dialog box can display URLs. The BIF_USENEWUI and BIF_BROWSEINCLUDEFILES flags must also be set. If any of these three flags are not set, the browser dialog box rejects URLs. Even when these flags are set, the browse dialog box displays URLs only if the folder that contains the selected item supports URLs. When the folder's <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a> method is called to request the selected item's attributes, the folder must set the <b>SFGAO_FOLDER</b> attribute flag. Otherwise, the browse dialog box will not display the URL.


##### - ulFlags.BIF_DONTGOBELOWDOMAIN (0x00000002)

0x00000002. Do not include network folders below the domain level in the dialog box's tree view control.


##### - ulFlags.BIF_EDITBOX (0x00000010)

0x00000010. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.71</a>. Include an edit control in the browse dialog box that allows the user to type the name of an item.


##### - ulFlags.BIF_NEWDIALOGSTYLE (0x00000040)

0x00000040. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. Use the new user interface. Setting this flag provides the user with a larger dialog box that can be resized. The dialog box has several new capabilities, including: drag-and-drop capability within the dialog box, reordering, shortcut menus, new folders, delete, and other shortcut menu commands.

                        

<div class="alert"><b>Note</b>  If COM is initialized through <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> with the COINIT_MULTITHREADED flag set, <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> fails if BIF_NEWDIALOGSTYLE is passed.</div>
<div> </div>

##### - ulFlags.BIF_NONEWFOLDERBUTTON (0x00000200)

0x00000200. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 6.0</a>. Do not include the <b>New Folder</b> button in the browse dialog box.


##### - ulFlags.BIF_NOTRANSLATETARGETS (0x00000400)

0x00000400. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 6.0</a>. When the selected item is a shortcut, return the PIDL of the shortcut itself rather than its target.


##### - ulFlags.BIF_RETURNFSANCESTORS (0x00000008)

0x00000008. Only return file system ancestors. An ancestor is a subfolder that is beneath the root folder in the namespace hierarchy. If the user selects an ancestor of the root folder that is not part of the file system, the <b>OK</b> button is grayed.


##### - ulFlags.BIF_RETURNONLYFSDIRS (0x00000001)

0x00000001. Only return file system directories. If the user selects folders that are not part of the file system, the <b>OK</b> button is grayed.

                        

<div class="alert"><b>Note</b>  The <b>OK</b> button remains enabled for "\\server" items, as well as "\\server\share" and directory items. However, if the user selects a "\\server" item, passing the PIDL returned by <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> to <a href="https://msdn.microsoft.com/f043ffa2-37c1-465d-aed6-0475e721fbde">SHGetPathFromIDList</a> fails.</div>
<div> </div>

##### - ulFlags.BIF_SHAREABLE (0x00008000)

0x00008000. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. The browse dialog box can display sharable resources on remote systems. This is intended for applications that want to expose remote shares on a local system. The BIF_NEWDIALOGSTYLE flag must also be set.


##### - ulFlags.BIF_STATUSTEXT (0x00000004)

0x00000004. Include a status area in the dialog box. The callback function can set the status text by sending messages to the dialog box. This flag is not supported when BIF_NEWDIALOGSTYLE is specified.


##### - ulFlags.BIF_UAHINT (0x00000100)

0x00000100. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 6.0</a>. When combined with BIF_NEWDIALOGSTYLE, adds a usage hint to the dialog box, in place of the edit box. BIF_EDITBOX overrides this flag.


##### - ulFlags.BIF_USENEWUI


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. Use the new user interface, including an edit box. This flag is equivalent to BIF_EDITBOX | BIF_NEWDIALOGSTYLE.

                        

<div class="alert"><b>Note</b>  If COM is initialized through <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> with the COINIT_MULTITHREADED flag set, <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> fails if BIF_USENEWUI is passed.</div>
<div> </div>

##### - ulFlags.BIF_VALIDATE (0x00000020)

0x00000020. <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.71</a>. If the user types an invalid name into the edit box, the browse dialog box calls the application's <a href="https://msdn.microsoft.com/e9109f38-34c7-46c0-aa0c-a6b4570f1c3a">BrowseCallbackProc</a> with the <b>BFFM_VALIDATEFAILED</b> message. This flag is ignored if BIF_EDITBOX is not specified.

