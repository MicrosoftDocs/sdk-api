---
UID: NF:wmsdkidl.IWMBackupRestoreProps.RemoveProp
title: IWMBackupRestoreProps::RemoveProp (wmsdkidl.h)
description: The RemoveProp method removes a property specified by name.
helpviewer_keywords: ["IWMBackupRestoreProps interface [windows Media Format]","RemoveProp method","IWMBackupRestoreProps.RemoveProp","IWMBackupRestoreProps::RemoveProp","IWMBackupRestorePropsRemoveProp","RemoveProp","RemoveProp method [windows Media Format]","RemoveProp method [windows Media Format]","IWMBackupRestoreProps interface","wmformat.iwmbackuprestoreprops_removeprop","wmsdkidl/IWMBackupRestoreProps::RemoveProp"]
old-location: wmformat\iwmbackuprestoreprops_removeprop.htm
tech.root: wmformat
ms.assetid: 3befd77c-6962-4320-9456-760e8f41cb24
ms.date: 12/05/2018
ms.keywords: IWMBackupRestoreProps interface [windows Media Format],RemoveProp method, IWMBackupRestoreProps.RemoveProp, IWMBackupRestoreProps::RemoveProp, IWMBackupRestorePropsRemoveProp, RemoveProp, RemoveProp method [windows Media Format], RemoveProp method [windows Media Format],IWMBackupRestoreProps interface, wmformat.iwmbackuprestoreprops_removeprop, wmsdkidl/IWMBackupRestoreProps::RemoveProp
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMBackupRestoreProps::RemoveProp
 - wmsdkidl/IWMBackupRestoreProps::RemoveProp
dev_langs:
 - c++
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
 - IWMBackupRestoreProps.RemoveProp
---

# IWMBackupRestoreProps::RemoveProp


## -description

<p class="CCE_Message">[<b>RemoveProp</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>RemoveProp</b> method removes a property specified by name.

## -parameters

### -param pcwszName [in]

Specifies the name of the property to be removed.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop">IWMBackupRestoreProps::SetProp</a>