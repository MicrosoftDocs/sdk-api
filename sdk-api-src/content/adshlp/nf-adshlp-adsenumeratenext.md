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

# ADsEnumerateNext function


## -description


The <b>ADsEnumerateNext</b> function enumerates through a specified number of elements from the current cursor position of the enumerator. When the operation succeeds, the function returns the enumerated set of elements in a variant array. The number of returned elements can be smaller than the specified number.


## -parameters




### -param pEnumVariant [in]

Type: <b>IEnumVARIANT*</b>

Pointer to the  <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface on the enumerator object.


### -param cElements [in]

Type: <b>ULONG</b>

Number of elements requested.


### -param pvar [out]

Type: <b>VARIANT*</b>

Pointer to the array of elements retrieved.


### -param pcElementsFetched [out]

Type: <b>ULONG*</b>

Actual number of elements retrieved, which can be smaller than the number of elements requested.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values.

For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The general process to enumerate objects in a container involves the following:

First, create an enumerator object on that container.

Second, retrieve the <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface pointer.

Third, call the <b>ADsEnumerateNext</b> function to return an enumerated set of elements from the enumerator object.

Fourth, call the <a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADSFreeEnumerator</a> function to free the enumerator object.

For more information and a code example, see the  <a href="https://msdn.microsoft.com/e4fdec19-bccf-49ec-8a95-29e096c4c9c1">ADsBuildEnumerator</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/e4fdec19-bccf-49ec-8a95-29e096c4c9c1">ADsBuildEnumerator</a>



<a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADsFreeEnumerator</a>



<a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>



<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

