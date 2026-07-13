---
UID: NF:wmsdkidl.IWMBackupRestoreProps.RemoveAllProps
title: IWMBackupRestoreProps::RemoveAllProps (wmsdkidl.h)
description: The RemoveAllProps method removes all properties.
helpviewer_keywords: ["IWMBackupRestoreProps interface [windows Media Format]","RemoveAllProps method","IWMBackupRestoreProps.RemoveAllProps","IWMBackupRestoreProps::RemoveAllProps","IWMBackupRestorePropsRemoveAllProps","RemoveAllProps","RemoveAllProps method [windows Media Format]","RemoveAllProps method [windows Media Format]","IWMBackupRestoreProps interface","wmformat.iwmbackuprestoreprops_removeallprops","wmsdkidl/IWMBackupRestoreProps::RemoveAllProps"]
old-location: wmformat\iwmbackuprestoreprops_removeallprops.htm
tech.root: wmformat
ms.assetid: 2c67eb68-1623-4aaa-abde-8481b77bd568
ms.date: 4/26/2023
ms.keywords: IWMBackupRestoreProps interface [windows Media Format],RemoveAllProps method, IWMBackupRestoreProps.RemoveAllProps, IWMBackupRestoreProps::RemoveAllProps, IWMBackupRestorePropsRemoveAllProps, RemoveAllProps, RemoveAllProps method [windows Media Format], RemoveAllProps method [windows Media Format],IWMBackupRestoreProps interface, wmformat.iwmbackuprestoreprops_removeallprops, wmsdkidl/IWMBackupRestoreProps::RemoveAllProps
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
 - IWMBackupRestoreProps::RemoveAllProps
 - wmsdkidl/IWMBackupRestoreProps::RemoveAllProps
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
 - IWMBackupRestoreProps.RemoveAllProps
---

# IWMBackupRestoreProps::RemoveAllProps


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>RemoveAllProps</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>RemoveAllProps</b> method removes all properties.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>
