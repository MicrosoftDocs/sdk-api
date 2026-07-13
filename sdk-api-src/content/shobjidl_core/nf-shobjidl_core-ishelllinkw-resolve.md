---
UID: NF:shobjidl_core.IShellLinkW.Resolve
title: IShellLinkW::Resolve (shobjidl_core.h)
description: Attempts to find the target of a Shell link, even if it has been moved or renamed. (Unicode)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","Resolve method","IShellLink::Resolve","IShellLinkA interface [Windows Shell]","Resolve method","IShellLinkA::Resolve","IShellLinkW interface [Windows Shell]","Resolve method","IShellLinkW.Resolve","IShellLinkW::Resolve","Resolve","Resolve method [Windows Shell]","Resolve method [Windows Shell]","IShellLink interface","Resolve method [Windows Shell]","IShellLinkA interface","Resolve method [Windows Shell]","IShellLinkW interface","SLR_ANY_MATCH","SLR_INVOKE_MSI","SLR_KNOWNFOLDER","SLR_MACHINE_IN_LOCAL_TARGET","SLR_NOLINKINFO","SLR_NOSEARCH","SLR_NOTRACK","SLR_NOUPDATE","SLR_NO_UI","SLR_NO_UI_WITH_MSG_PUMP","SLR_OFFER_DELETE_WITHOUT_FILE","SLR_UPDATE","SLR_UPDATE_MACHINE_AND_SID","_win32_IShellLink_Resolve","shell.IShellLink_Resolve","shobjidl_core/IShellLink::Resolve","shobjidl_core/IShellLinkA::Resolve","shobjidl_core/IShellLinkW::Resolve"]
old-location: shell\IShellLink_Resolve.htm
tech.root: shell
ms.assetid: a31f1d6d-7b87-4777-89a8-a032b7629b7e
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],Resolve method, IShellLink::Resolve, IShellLinkA interface [Windows Shell],Resolve method, IShellLinkA::Resolve, IShellLinkW interface [Windows Shell],Resolve method, IShellLinkW.Resolve, IShellLinkW::Resolve, Resolve, Resolve method [Windows Shell], Resolve method [Windows Shell],IShellLink interface, Resolve method [Windows Shell],IShellLinkA interface, Resolve method [Windows Shell],IShellLinkW interface, SLR_ANY_MATCH, SLR_INVOKE_MSI, SLR_KNOWNFOLDER, SLR_MACHINE_IN_LOCAL_TARGET, SLR_NOLINKINFO, SLR_NOSEARCH, SLR_NOTRACK, SLR_NOUPDATE, SLR_NO_UI, SLR_NO_UI_WITH_MSG_PUMP, SLR_OFFER_DELETE_WITHOUT_FILE, SLR_UPDATE, SLR_UPDATE_MACHINE_AND_SID, _win32_IShellLink_Resolve, shell.IShellLink_Resolve, shobjidl_core/IShellLink::Resolve, shobjidl_core/IShellLinkA::Resolve, shobjidl_core/IShellLinkW::Resolve
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkW::Resolve
 - shobjidl_core/IShellLinkW::Resolve
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLink.Resolve
 - IShellLinkA.Resolve
 - IShellLinkW.Resolve
---

# IShellLinkW::Resolve


## -description

Attempts to find the target of a Shell link, even if it has been moved or renamed.

## -parameters

### -param hwnd

Type: <b>HWND</b>

A handle to the window that the Shell will use as the parent for a dialog box. The Shell displays the dialog box if it needs to prompt the user for more information while resolving a Shell link.

### -param fFlags

Type: <b>DWORD</b>

Action flags. This parameter can be a combination of the following values.



#### SLR_NO_UI (0x0001)

0x0001. Do not display a dialog box if the link cannot be resolved. When <b>SLR_NO_UI</b> is set, the high-order word of <i>fFlags</i> can be set to a time-out value that specifies the maximum amount of time to be spent resolving the link. The function returns if the link cannot be resolved within the time-out duration. If the high-order word is set to zero, the time-out duration will be set to the default value of 3,000 milliseconds (3 seconds). To specify a value, set the high word of <i>fFlags</i> to the desired time-out duration, in milliseconds.



#### SLR_ANY_MATCH (0x0002)

0x0002. Not used.



#### SLR_UPDATE (0x0004)

0x0004. If the link object has changed, update its path and list of identifiers. If <b>SLR_UPDATE</b> is set, you do not need to call <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-isdirty">IPersistFile::IsDirty</a> to determine whether the link object has changed.



#### SLR_NOUPDATE (0x0008)

0x0008. Do not update the link information.



#### SLR_NOSEARCH (0x0010)

0x0010. Do not execute the search heuristics.



#### SLR_NOTRACK (0x0020)

0x0020. Do not use distributed link tracking.



#### SLR_NOLINKINFO (0x0040)

0x0040. Disable distributed link tracking. By default, distributed link tracking tracks removable media across multiple devices based on the volume name. It also uses the UNC path to track remote file systems whose drive letter has changed. Setting <b>SLR_NOLINKINFO</b> disables both types of tracking.



#### SLR_INVOKE_MSI (0x0080)

0x0080. Call the Windows Installer.



#### SLR_NO_UI_WITH_MSG_PUMP (0x0101)

0x0101. <b>Windows XP and later</b>. 



#### SLR_OFFER_DELETE_WITHOUT_FILE (0x0200)

0x0200. <b>Windows 7 and later</b>. Offer the option to delete the shortcut when this method is unable to resolve it, even if the shortcut is not a shortcut to a file.



#### SLR_KNOWNFOLDER (0x0400)

0x0400. <b>Windows 7 and later</b>. Report as dirty if the target is a known folder and the known folder was redirected. This only works if the original target path was a file system path or ID list and not an aliased known folder ID list.



#### SLR_MACHINE_IN_LOCAL_TARGET (0x0800)

0x0800. <b>Windows 7 and later</b>. Resolve the computer name in UNC targets that point to a local computer. This value is used with <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags">SLDF_KEEP_LOCAL_IDLIST_FOR_UNC_TARGET</a>.



#### SLR_UPDATE_MACHINE_AND_SID (0x1000)

0x1000. <b>Windows 7 and later</b>. Update the computer GUID and user SID if necessary.


##### - fFlags.SLR_ANY_MATCH (0x0002)

0x0002. Not used.


##### - fFlags.SLR_INVOKE_MSI (0x0080)

0x0080. Call the Windows Installer.


##### - fFlags.SLR_KNOWNFOLDER (0x0400)

0x0400. <b>Windows 7 and later</b>. Report as dirty if the target is a known folder and the known folder was redirected. This only works if the original target path was a file system path or ID list and not an aliased known folder ID list.


##### - fFlags.SLR_MACHINE_IN_LOCAL_TARGET (0x0800)

0x0800. <b>Windows 7 and later</b>. Resolve the computer name in UNC targets that point to a local computer. This value is used with <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags">SLDF_KEEP_LOCAL_IDLIST_FOR_UNC_TARGET</a>.


##### - fFlags.SLR_NOLINKINFO (0x0040)

0x0040. Disable distributed link tracking. By default, distributed link tracking tracks removable media across multiple devices based on the volume name. It also uses the UNC path to track remote file systems whose drive letter has changed. Setting <b>SLR_NOLINKINFO</b> disables both types of tracking.


##### - fFlags.SLR_NOSEARCH (0x0010)

0x0010. Do not execute the search heuristics.


##### - fFlags.SLR_NOTRACK (0x0020)

0x0020. Do not use distributed link tracking.


##### - fFlags.SLR_NOUPDATE (0x0008)

0x0008. Do not update the link information.


##### - fFlags.SLR_NO_UI (0x0001)

0x0001. Do not display a dialog box if the link cannot be resolved. When <b>SLR_NO_UI</b> is set, the high-order word of <i>fFlags</i> can be set to a time-out value that specifies the maximum amount of time to be spent resolving the link. The function returns if the link cannot be resolved within the time-out duration. If the high-order word is set to zero, the time-out duration will be set to the default value of 3,000 milliseconds (3 seconds). To specify a value, set the high word of <i>fFlags</i> to the desired time-out duration, in milliseconds.


##### - fFlags.SLR_NO_UI_WITH_MSG_PUMP (0x0101)

0x0101. <b>Windows XP and later</b>. 


##### - fFlags.SLR_OFFER_DELETE_WITHOUT_FILE (0x0200)

0x0200. <b>Windows 7 and later</b>. Offer the option to delete the shortcut when this method is unable to resolve it, even if the shortcut is not a shortcut to a file.


##### - fFlags.SLR_UPDATE (0x0004)

0x0004. If the link object has changed, update its path and list of identifiers. If <b>SLR_UPDATE</b> is set, you do not need to call <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-isdirty">IPersistFile::IsDirty</a> to determine whether the link object has changed.


##### - fFlags.SLR_UPDATE_MACHINE_AND_SID (0x1000)

0x1000. <b>Windows 7 and later</b>. Update the computer GUID and user SID if necessary.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Following link creation, the name or location of the target may change. The <b>IShellLink::Resolve</b> method first retrieves the path associated with the link. If the object is no longer there or has been renamed, <b>Resolve</b> will attempt to find it. If successful, and the following conditions are met, the file that the link object was loaded from will be updated to reflect the new state of the link object.

<ul>
<li>The <b>SLR_UPDATE</b> flag is set.</li>
<li>The target has been moved or renamed, updating the internal state of the Shell link object to refer to the new target.</li>
<li>The Shell link object was loaded from a file through <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>.</li>
</ul>
The client can also call the <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-isdirty">IPersistFile::IsDirty</a> method to determine whether the link object has changed and the file needs to be updated.

<b>Resolve</b> has two approaches to finding target objects. The first is the distributed link tracking service. If the service is available, it can find an object that was on an NTFS version 5.0 volume and was moved to another location on that volume. It can also find an object that was moved to another NTFS version 5.0 volume, including volumes on other computers. To suppress the use of this service, set the <b>SLR_NOTRACK</b> flag.

If distributed link tracking is not available or fails to find the link object, <b>Resolve</b> attempts to find it with search heuristics. It first looks in the object's last known directory for an object with a different name but the same attributes and file creation time. Next, it recursively searches subdirectories in the vicinity of the object's last known directory. It looks for an object with the same name or creation time. Finally, <b>Resolve</b> looks for a matching object on the desktop and other local volumes. To suppress the use of the search heuristics, set the <b>SLR_NOSEARCH</b> flag.

If both approaches fail, the system will display a dialog box prompting the user for a location. To suppress the dialog box, set the <b>SLR_NO_UI</b> flag.
