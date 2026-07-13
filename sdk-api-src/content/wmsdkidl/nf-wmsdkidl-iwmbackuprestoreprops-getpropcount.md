---
UID: NF:wmsdkidl.IWMBackupRestoreProps.GetPropCount
title: IWMBackupRestoreProps::GetPropCount (wmsdkidl.h)
description: The GetPropCount method retrieves the number of properties.
helpviewer_keywords: ["GetPropCount","GetPropCount method [windows Media Format]","GetPropCount method [windows Media Format]","IWMBackupRestoreProps interface","IWMBackupRestoreProps interface [windows Media Format]","GetPropCount method","IWMBackupRestoreProps.GetPropCount","IWMBackupRestoreProps::GetPropCount","IWMBackupRestorePropsGetPropCount","wmformat.iwmbackuprestoreprops_getpropcount","wmsdkidl/IWMBackupRestoreProps::GetPropCount"]
old-location: wmformat\iwmbackuprestoreprops_getpropcount.htm
tech.root: wmformat
ms.assetid: 70b8dcf7-e48b-4c1e-be39-d0ae3c8a2b23
ms.date: 4/26/2023
ms.keywords: GetPropCount, GetPropCount method [windows Media Format], GetPropCount method [windows Media Format],IWMBackupRestoreProps interface, IWMBackupRestoreProps interface [windows Media Format],GetPropCount method, IWMBackupRestoreProps.GetPropCount, IWMBackupRestoreProps::GetPropCount, IWMBackupRestorePropsGetPropCount, wmformat.iwmbackuprestoreprops_getpropcount, wmsdkidl/IWMBackupRestoreProps::GetPropCount
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
 - IWMBackupRestoreProps::GetPropCount
 - wmsdkidl/IWMBackupRestoreProps::GetPropCount
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
 - IWMBackupRestoreProps.GetPropCount
---

# IWMBackupRestoreProps::GetPropCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetPropCount</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetPropCount</b> method retrieves the number of properties.



This method is not implemented.

## -parameters

### -param pcProps [out]

Pointer to a count of the properties.

## -returns

The method returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop">IWMBackupRestoreProps::SetProp</a>