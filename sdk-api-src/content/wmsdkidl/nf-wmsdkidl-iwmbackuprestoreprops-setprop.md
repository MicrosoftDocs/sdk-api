---
UID: NF:wmsdkidl.IWMBackupRestoreProps.SetProp
title: IWMBackupRestoreProps::SetProp (wmsdkidl.h)
description: The SetProp method adds a property, and specifies its name and value.
helpviewer_keywords: ["IWMBackupRestoreProps interface [windows Media Format]","SetProp method","IWMBackupRestoreProps.SetProp","IWMBackupRestoreProps::SetProp","IWMBackupRestorePropsSetProp","SetProp","SetProp method [windows Media Format]","SetProp method [windows Media Format]","IWMBackupRestoreProps interface","wmformat.iwmbackuprestoreprops_setprop","wmsdkidl/IWMBackupRestoreProps::SetProp"]
old-location: wmformat\iwmbackuprestoreprops_setprop.htm
tech.root: wmformat
ms.assetid: 582c1590-8855-409c-9964-a0fb7baa05bd
ms.date: 4/26/2023
ms.keywords: IWMBackupRestoreProps interface [windows Media Format],SetProp method, IWMBackupRestoreProps.SetProp, IWMBackupRestoreProps::SetProp, IWMBackupRestorePropsSetProp, SetProp, SetProp method [windows Media Format], SetProp method [windows Media Format],IWMBackupRestoreProps interface, wmformat.iwmbackuprestoreprops_setprop, wmsdkidl/IWMBackupRestoreProps::SetProp
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
 - IWMBackupRestoreProps::SetProp
 - wmsdkidl/IWMBackupRestoreProps::SetProp
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
 - IWMBackupRestoreProps.SetProp
---

# IWMBackupRestoreProps::SetProp


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>SetProp</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>SetProp</b> method adds a property, and specifies its name and value.

## -parameters

### -param pszName [in]

Pointer to a null-terminated string containing the name.

### -param Type [in]

Pointer to a variable containing one member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type. The current implementation of this method accepts only WMT_TYPE_STRING. Specifying a different type causes the method to return E_INVALIDARG.

### -param pValue [in]

Pointer to a byte array containing the value of the property.

### -param cbLength [in]

Length of <i>pValue</i>, in bytes.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used to set properties that are needed by the other backup restorer object interfaces.

The following table lists the predefined properties.

<table>
<tr>
<th>Property name
            </th>
<th>Type
            </th>
<th>Description
            </th>
</tr>
<tr>
<td><b>BackupPath</b></td>
<td><b>String</b></td>
<td>Full path to the location where the backup files must be saved.</td>
</tr>
<tr>
<td><b>RestorePath</b></td>
<td><b>String</b></td>
<td>Full path to the location where the backup files can be found and used to restore data.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup">IWMLicenseBackup Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore">IWMLicenseRestore Interface</a>