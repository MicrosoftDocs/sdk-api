---
UID: NF:shlobj_core.IExtractIconW.GetIconLocation
title: IExtractIconW::GetIconLocation (shlobj_core.h)
description: Gets the location and index of an icon. (Unicode)
helpviewer_keywords: ["GIL_ASYNC","GIL_CHECKSHIELD","GIL_DEFAULTICON","GIL_DONTCACHE","GIL_FORCENOSHIELD","GIL_FORSHELL","GIL_FORSHORTCUT","GIL_NOTFILENAME","GIL_OPENICON","GIL_PERCLASS","GIL_PERINSTANCE","GIL_SHIELD","GIL_SIMULATEDOC","GetIconLocation","GetIconLocation method [Windows Shell]","GetIconLocation method [Windows Shell]","IExtractIcon interface","IExtractIcon interface [Windows Shell]","GetIconLocation method","IExtractIcon::GetIconLocation","IExtractIconA","IExtractIconA::GetIconLocation","IExtractIconW","IExtractIconW.GetIconLocation","IExtractIconW::GetIconLocation","_win32_IExtractIcon_GetIconLocation","shell.IExtractIcon_GetIconLocation","shlobj_core/IExtractIcon::GetIconLocation"]
old-location: shell\IExtractIcon_GetIconLocation.htm
tech.root: shell
ms.assetid: 56138982-c062-4b07-aea7-6023037451fe
ms.date: 12/05/2018
ms.keywords: GIL_ASYNC, GIL_CHECKSHIELD, GIL_DEFAULTICON, GIL_DONTCACHE, GIL_FORCENOSHIELD, GIL_FORSHELL, GIL_FORSHORTCUT, GIL_NOTFILENAME, GIL_OPENICON, GIL_PERCLASS, GIL_PERINSTANCE, GIL_SHIELD, GIL_SIMULATEDOC, GetIconLocation, GetIconLocation method [Windows Shell], GetIconLocation method [Windows Shell],IExtractIcon interface, IExtractIcon interface [Windows Shell],GetIconLocation method, IExtractIcon::GetIconLocation, IExtractIconA, IExtractIconA::GetIconLocation, IExtractIconW, IExtractIconW.GetIconLocation, IExtractIconW::GetIconLocation, _win32_IExtractIcon_GetIconLocation, shell.IExtractIcon_GetIconLocation, shlobj_core/IExtractIcon::GetIconLocation
req.header: shlobj_core.h
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
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtractIconW::GetIconLocation
 - shlobj_core/IExtractIconW::GetIconLocation
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
 - IExtractIcon.GetIconLocation
 - IExtractIconA::GetIconLocation
 - IExtractIconW::GetIconLocation
---

# IExtractIconW::GetIconLocation


## -description

Gets the location and index of an icon.

## -parameters

### -param uFlags

Type: <b>UINT</b>

One or more of the following values. This parameter can also be <b>NULL</b>.



#### GIL_ASYNC (0x0020)

Set this flag to determine whether the icon should be extracted asynchronously. If the icon can be extracted rapidly, this flag is usually ignored. If extraction will take more time, <b>GetIconLocation</b> should return E_PENDING. See the Remarks for further discussion.



#### GIL_DEFAULTICON (0x0040)

Retrieve information about the fallback icon. Fallback icons are usually used while the desired icon is extracted and added to the cache.



#### GIL_FORSHELL (0x0002)

The icon is displayed in a Shell folder.



#### GIL_FORSHORTCUT (0x0080)

The icon indicates a shortcut. However, the icon extractor should not apply the shortcut overlay; that will be done later. Shortcut icons are state-independent.



#### GIL_OPENICON (0x0001)

The icon is in the open state if both open-state and closed-state images are available. If this flag is not specified, the icon is in the normal or closed state. This flag is typically used for folder objects.



#### GIL_CHECKSHIELD (0x0200)

Explicitly return either GIL_SHIELD or GIL_FORCENOSHIELD in <i>pwFlags</i>. Do not block if GIL_ASYNC is set.

### -param pszIconFile [out]

Type: <b>PTSTR</b>

A pointer to a buffer that receives the icon location. The icon location is a null-terminated string that identifies the file that contains the icon.

### -param cchMax

Type: <b>UINT</b>

The size of the buffer, in characters, pointed to by <i>pszIconFile</i>.

### -param piIndex [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that receives the index of the icon in the file pointed to by <i>pszIconFile</i>.

### -param pwFlags [out]

Type: <b>UINT*</b>

A pointer to a <b>UINT</b> value that receives zero or a combination of the following values.



#### GIL_DONTCACHE (0x0010)

The physical image bits for this icon are not cached by the calling application.



#### GIL_NOTFILENAME (0x0008)

The location is not a file name/index pair. The values in <i>pszIconFile</i> and <i>piIndex</i> cannot be passed to <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a> or <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a>.

When this flag is omitted, the value returned in <i>pszIconFile</i> is a fully-qualified path name to either a .ico file or to a file that can contain icons. Also, the value returned in <i>piIndex</i> is an index into that file that identifies which of its icons to use. Therefore, when the GIL_NOTFILENAME flag is omitted, these values can be passed to <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a> or <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a>.



#### GIL_PERCLASS (0x0004)

All objects of this class have the same icon. This flag is used internally by the Shell. Typical implementations of <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a> do not require this flag because the flag implies that an icon handler is not required to resolve the icon on a per-object basis. The recommended method for implementing per-class icons is to register a DefaultIcon for the class.



#### GIL_PERINSTANCE (0x0002)

Each object of this class has its own icon. This flag is used internally by the Shell to handle cases like Setup.exe, where objects with identical names can have different icons. Typical implementations of <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a> do not require this flag.



#### GIL_SIMULATEDOC (0x0001)

The calling application should create a document icon using the specified icon.



#### GIL_SHIELD (0x0200)

<b>Windows Vista only</b>. The calling application must stamp the icon with the UAC shield.



#### GIL_FORCENOSHIELD (0x0400)

<b>Windows Vista only</b>. The calling application must not stamp the icon with the UAC shield.


##### - pwFlags.GIL_DONTCACHE (0x0010)

The physical image bits for this icon are not cached by the calling application.


##### - pwFlags.GIL_FORCENOSHIELD (0x0400)

<b>Windows Vista only</b>. The calling application must not stamp the icon with the UAC shield.


##### - pwFlags.GIL_NOTFILENAME (0x0008)

The location is not a file name/index pair. The values in <i>pszIconFile</i> and <i>piIndex</i> cannot be passed to <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a> or <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a>.

When this flag is omitted, the value returned in <i>pszIconFile</i> is a fully-qualified path name to either a .ico file or to a file that can contain icons. Also, the value returned in <i>piIndex</i> is an index into that file that identifies which of its icons to use. Therefore, when the GIL_NOTFILENAME flag is omitted, these values can be passed to <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a> or <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a>.


##### - pwFlags.GIL_PERCLASS (0x0004)

All objects of this class have the same icon. This flag is used internally by the Shell. Typical implementations of <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a> do not require this flag because the flag implies that an icon handler is not required to resolve the icon on a per-object basis. The recommended method for implementing per-class icons is to register a DefaultIcon for the class.


##### - pwFlags.GIL_PERINSTANCE (0x0002)

Each object of this class has its own icon. This flag is used internally by the Shell to handle cases like Setup.exe, where objects with identical names can have different icons. Typical implementations of <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a> do not require this flag.


##### - pwFlags.GIL_SHIELD (0x0200)

<b>Windows Vista only</b>. The calling application must stamp the icon with the UAC shield.


##### - pwFlags.GIL_SIMULATEDOC (0x0001)

The calling application should create a document icon using the specified icon.


##### - uFlags.GIL_ASYNC (0x0020)

Set this flag to determine whether the icon should be extracted asynchronously. If the icon can be extracted rapidly, this flag is usually ignored. If extraction will take more time, <b>GetIconLocation</b> should return E_PENDING. See the Remarks for further discussion.


##### - uFlags.GIL_CHECKSHIELD (0x0200)

Explicitly return either GIL_SHIELD or GIL_FORCENOSHIELD in <i>pwFlags</i>. Do not block if GIL_ASYNC is set.


##### - uFlags.GIL_DEFAULTICON (0x0040)

Retrieve information about the fallback icon. Fallback icons are usually used while the desired icon is extracted and added to the cache.


##### - uFlags.GIL_FORSHELL (0x0002)

The icon is displayed in a Shell folder.


##### - uFlags.GIL_FORSHORTCUT (0x0080)

The icon indicates a shortcut. However, the icon extractor should not apply the shortcut overlay; that will be done later. Shortcut icons are state-independent.


##### - uFlags.GIL_OPENICON (0x0001)

The icon is in the open state if both open-state and closed-state images are available. If this flag is not specified, the icon is in the normal or closed state. This flag is typically used for folder objects.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the function returned a valid location, or S_FALSE if the Shell should use a default icon. If the <b>GIL_ASYNC</b> flag is set in <i>uFlags</i>, the method can return E_PENDING to indicate that icon extraction will be time-consuming.

## -remarks

When a client sets the <b>GIL_ASYNC</b> flag in <i>uFlags</i> and receives E_PENDING as a return value, it typically creates a background thread to extract the icon. It calls <b>GetIconLocation</b> from that thread, without the <b>GIL_ASYNC</b> flag, to retrieve the icon location. It then calls <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-extract">IExtractIcon::Extract</a> to extract the icon. Returning E_PENDING implies that the object is free threaded. In other words, it can safely be called concurrently by multiple threads.

The <b>GIL_DEFAULTICON</b> flag is usually set in the case where the desired icon is found, but that icon is not present in the icon cache. Icon extraction is a low priority background process, and as such may be delayed by other processes. The default icon will be displayed in place of the final icon during the time that it takes for that final icon to be extracted, added to the cache, and made available.
