---
UID: NF:wmsdkidl.IWMBackupRestoreProps.SetProp
title: IWMBackupRestoreProps::SetProp
author: windows-sdk-content
description: The SetProp method adds a property, and specifies its name and value.
old-location: wmformat\iwmbackuprestoreprops_setprop.htm
old-project: wmformat
ms.assetid: 582c1590-8855-409c-9964-a0fb7baa05bd
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMBackupRestoreProps interface [windows Media Format],SetProp method, IWMBackupRestoreProps.SetProp, IWMBackupRestoreProps::SetProp, IWMBackupRestorePropsSetProp, SetProp, SetProp method [windows Media Format], SetProp method [windows Media Format],IWMBackupRestoreProps interface, wmformat.iwmbackuprestoreprops_setprop, wmsdkidl/IWMBackupRestoreProps::SetProp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMBackupRestoreProps::SetProp


## -description


<p class="CCE_Message">[<b>SetProp</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>SetProp</b> method adds a property, and specifies its name and value.




## -parameters




### -param pszName [in]

Pointer to a null-terminated string containing the name.


### -param Type [in]

Pointer to a variable containing one member of the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type. The current implementation of this method accepts only WMT_TYPE_STRING. Specifying a different type causes the method to return E_INVALIDARG.


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
<th>
              Property name
            </th>
<th>
              Type
            </th>
<th>
              Description
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




<a href="https://msdn.microsoft.com/3a5af1f3-e652-4729-931b-d0702af408f3">IWMBackupRestoreProps Interface</a>



<a href="https://msdn.microsoft.com/4ef43b7e-706b-48f6-80ba-7d0a59c3929a">IWMLicenseBackup Interface</a>



<a href="https://msdn.microsoft.com/29444445-7104-4900-a00d-dabd2766d1d7">IWMLicenseRestore Interface</a>
 

 

