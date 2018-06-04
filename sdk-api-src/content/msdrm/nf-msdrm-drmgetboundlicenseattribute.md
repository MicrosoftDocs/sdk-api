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

# DRMGetBoundLicenseAttribute function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetBoundLicenseAttribute</b> function retrieves a bound license attribute from the license XrML.


## -parameters




### -param hQueryRoot [in]

A handle to a root query object, from a previous call to this function or from <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>.


### -param wszAttribute [in]

The attribute to retrieve.


### -param iWhich [in]

Zero-based index of the occurrence to retrieve.


### -param peEncoding [out]

Encoding type used.


### -param pcBuffer [in, out]

Size, in characters, of the attribute retrieved plus one for a terminating null character.


### -param pbBuffer [out]

Pointer to the attribute object.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The Active Directory Rights Management system exposes an object-oriented interface to the underlying license XrML. This function, along with other <b>DRMGetBoundLicense_xxx</b> functions, allows an application to navigate this structure.

Attributes hold information about an object, such as its name, issue time, or SKU value. To obtain attribute information, you must first determine the size of the buffer needed to hold the retrieved information by calling the function with <b>NULL</b> in the <i>pbBuffer</i> value. If the function succeeds and returns a value in <i>pcBuffer</i>, then allocate a properly sized buffer by using this value and call the function again, passing in to <i>pbBuffer</i> the allocated buffer to receive the value of the attribute.

An object can have several instances of an attribute with the same name. For example, there can be several authenticator type values in a license. In this case, it may be necessary to iterate through all the instances of an attribute by first calling <a href="https://msdn.microsoft.com/5b3814f5-bab7-4b46-a38b-54406cb8cae0">DRMGetBoundLicenseAttributeCount</a> to get a count of existing objects and then looping through all <i>iWhich</i> instances of the attribute, starting at zero and incrementing by one.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/5b3814f5-bab7-4b46-a38b-54406cb8cae0">DRMGetBoundLicenseAttributeCount</a>



<a href="https://msdn.microsoft.com/d1be0668-fb5a-4541-92dc-34255ba3fdad">DRMGetBoundLicenseObject</a>



<a href="https://msdn.microsoft.com/1bb9a9b7-f254-4c2b-a7b0-5e9b99c92488">DRMGetBoundLicenseObjectCount</a>
 

 

