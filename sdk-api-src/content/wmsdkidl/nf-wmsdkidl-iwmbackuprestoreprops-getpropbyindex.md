---
UID: NF:wmsdkidl.IWMBackupRestoreProps.GetPropByIndex
title: IWMBackupRestoreProps::GetPropByIndex (wmsdkidl.h)
description: The GetPropByIndex method retrieves the name and value of a property by index.
helpviewer_keywords: ["GetPropByIndex","GetPropByIndex method [windows Media Format]","GetPropByIndex method [windows Media Format]","IWMBackupRestoreProps interface","IWMBackupRestoreProps interface [windows Media Format]","GetPropByIndex method","IWMBackupRestoreProps.GetPropByIndex","IWMBackupRestoreProps::GetPropByIndex","IWMBackupRestorePropsGetPropByIndex","wmformat.iwmbackuprestoreprops_getpropbyindex","wmsdkidl/IWMBackupRestoreProps::GetPropByIndex"]
old-location: wmformat\iwmbackuprestoreprops_getpropbyindex.htm
tech.root: wmformat
ms.assetid: 96376e63-3c36-4bea-8cd2-362bb1ba054f
ms.date: 4/26/2023
ms.keywords: GetPropByIndex, GetPropByIndex method [windows Media Format], GetPropByIndex method [windows Media Format],IWMBackupRestoreProps interface, IWMBackupRestoreProps interface [windows Media Format],GetPropByIndex method, IWMBackupRestoreProps.GetPropByIndex, IWMBackupRestoreProps::GetPropByIndex, IWMBackupRestorePropsGetPropByIndex, wmformat.iwmbackuprestoreprops_getpropbyindex, wmsdkidl/IWMBackupRestoreProps::GetPropByIndex
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
 - IWMBackupRestoreProps::GetPropByIndex
 - wmsdkidl/IWMBackupRestoreProps::GetPropByIndex
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
 - IWMBackupRestoreProps.GetPropByIndex
---

# IWMBackupRestoreProps::GetPropByIndex


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetPropByIndex</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetPropByIndex</b> method retrieves the name and value of a property by index.



This method is not implemented.

## -parameters

### -param wIndex [in]

<b>WORD</b> containing the index of the property.

### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name.

### -param pcchNameLen [in, out]

On input, contains the length of <i>pwszName</i>. On output, points to a variable containing the number of characters in <i>pwszName</i>, including the terminating <b>null</b> character.

### -param pType [out]

Pointer to a variable containing one member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type.

### -param pValue [out]

Pointer to a byte array containing the value of the property.

### -param pcbLength [in, out]

On input, contains the length of <i>pValue</i>. On output, points to a count of the bytes in <i>pValue</i> that are used.

## -returns

The method returns E_NOTIMPL.

## -remarks

You should make two calls to <b>GetPropByIndex</b>. On the first call, pass <b>NULL</b> for <i>pwszName</i> and <i>pValue</i>. On return, the value pointed to by <i>pcchNameLen</i> is set to the length in wide characters of the property name (including the terminating <b>null</b> character) and the value pointed to by <i>pcbLength</i> is set to the number of bytes required to hold the property value. You can then allocate buffers of the appropriate sizes to hold the values <i>pwszName</i> and <i>pValue</i> and pass pointers to them on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop">IWMBackupRestoreProps::SetProp</a>