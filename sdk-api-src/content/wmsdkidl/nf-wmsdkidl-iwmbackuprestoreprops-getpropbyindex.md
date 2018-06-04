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

# IWMBackupRestoreProps::GetPropByIndex


## -description


<p class="CCE_Message">[<b>GetPropByIndex</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
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

Pointer to a variable containing one member of the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type.


### -param pValue [out]

Pointer to a byte array containing the value of the property.


### -param pcbLength [in, out]

On input, contains the length of <i>pValue</i>. On output, points to a count of the bytes in <i>pValue</i> that are used.


## -returns



The method returns E_NOTIMPL.




## -remarks



You should make two calls to <b>GetPropByIndex</b>. On the first call, pass <b>NULL</b> for <i>pwszName</i> and <i>pValue</i>. On return, the value pointed to by <i>pcchNameLen</i> is set to the length in wide characters of the property name (including the terminating <b>null</b> character) and the value pointed to by <i>pcbLength</i> is set to the number of bytes required to hold the property value. You can then allocate buffers of the appropriate sizes to hold the values <i>pwszName</i> and <i>pValue</i> and pass pointers to them on the second call.




## -see-also




<a href="https://msdn.microsoft.com/3a5af1f3-e652-4729-931b-d0702af408f3">IWMBackupRestoreProps Interface</a>



<a href="https://msdn.microsoft.com/582c1590-8855-409c-9964-a0fb7baa05bd">IWMBackupRestoreProps::SetProp</a>
 

 

