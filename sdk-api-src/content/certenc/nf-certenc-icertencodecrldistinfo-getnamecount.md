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

# ICertEncodeCRLDistInfo::GetNameCount


## -description


The <b>GetNameCount</b> method returns the number of names in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution point.


## -parameters




### -param DistPointIndex [in]

Specifies the index of the distribution point for which to get the name count.


### -param pNameCount [out]

A pointer to a <b>Long</b> that will represent the number of name values contained in the CRL distribution point.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of names in the CRL distribution point.




## -see-also




<a href="https://msdn.microsoft.com/e9c0053f-263f-4d7b-9356-bc33af989dbe">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/8c7d0d14-e755-4223-8cd5-0ebc784960cf">ICertEncodeCRLDistInfo::GetDistPointCount</a>



<a href="https://msdn.microsoft.com/a564af61-fb5e-46b7-a818-333b4d5e2f25">ICertEncodeCRLDistInfo::GetName</a>



<a href="https://msdn.microsoft.com/ce27adfd-e21a-4e8d-882e-72041f97958a">ICertEncodeCRLDistInfo::SetNameCount</a>
 

 

