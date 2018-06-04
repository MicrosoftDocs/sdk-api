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
 

 

