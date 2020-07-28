---
UID: NF:wmsdkidl.IWMLicenseRestore.RestoreLicenses
title: IWMLicenseRestore::RestoreLicenses (wmsdkidl.h)
description: The RestoreLicenses method restores licenses that were previously backed up.
helpviewer_keywords: ["IWMLicenseRestore interface [windows Media Format]","RestoreLicenses method","IWMLicenseRestore.RestoreLicenses","IWMLicenseRestore::RestoreLicenses","IWMLicenseRestoreRestoreLicenses","RestoreLicenses","RestoreLicenses method [windows Media Format]","RestoreLicenses method [windows Media Format]","IWMLicenseRestore interface","wmformat.iwmlicenserestore_restorelicenses","wmsdkidl/IWMLicenseRestore::RestoreLicenses"]
old-location: wmformat\iwmlicenserestore_restorelicenses.htm
tech.root: wmformat
ms.assetid: 2d645b3a-e856-4745-b80a-89a3bc2b38bd
ms.date: 12/05/2018
ms.keywords: IWMLicenseRestore interface [windows Media Format],RestoreLicenses method, IWMLicenseRestore.RestoreLicenses, IWMLicenseRestore::RestoreLicenses, IWMLicenseRestoreRestoreLicenses, RestoreLicenses, RestoreLicenses method [windows Media Format], RestoreLicenses method [windows Media Format],IWMLicenseRestore interface, wmformat.iwmlicenserestore_restorelicenses, wmsdkidl/IWMLicenseRestore::RestoreLicenses
f1_keywords:
- wmsdkidl/IWMLicenseRestore.RestoreLicenses
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmvcore.lib
- Wmvcore.dll
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMLicenseRestore.RestoreLicenses
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMLicenseRestore::RestoreLicenses


## -description


<p class="CCE_Message">[<b>RestoreLicenses</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>RestoreLicenses</b> method restores licenses that were previously backed up.




## -parameters




### -param dwFlags [in]

<b>DWORD</b> containing the flags.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WM_RESTORE_INDIVIDUALIZE</td>
<td>Indicates that the application has received permission from the user to individualize their computer. (See <a href="https://docs.microsoft.com/windows/desktop/wmformat/individualizing-drm-applications">Individualizing DRM Applications</a> section.)</td>
</tr>
</table>
 


### -param pCallback [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



For more information on how to specify the location of the backup file (there are predefined properties for the backup path and restore path for this purpose), see <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>.

The operation of this method is asynchronous, and an <b>IWMStatusCallback</b> interface can be used to track progress.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore">IWMLicenseRestore Interface</a>
 

 

