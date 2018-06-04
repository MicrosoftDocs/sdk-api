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

# __MIDL___MIDL_itf_ads_0000_0000_0027 enumeration


## -description


The <b>ADS_PROPERTY_OPERATION_ENUM</b> enumeration specifies ways to update a named property in the cache.


## -enum-fields




### -field ADS_PROPERTY_CLEAR

Instructs the directory service to remove all the property value(s) from the object.


### -field ADS_PROPERTY_UPDATE

Instructs the directory service to replace the current value(s) with the specified value(s).


### -field ADS_PROPERTY_APPEND

Instructs the directory service to append the specified value(s) to the existing values(s).

When the <b>ADS_PROPERTY_APPEND</b> operation is specified, the new attribute value(s) are automatically committed to the directory service and removed from the local cache. This forces the local cache to be updated from the directory service the next time the attribute value(s) are retrieved.


### -field ADS_PROPERTY_DELETE

Instructs the directory service to delete the specified value(s) from the object.


## -remarks



The elements of this enumeration are used with the  <a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs.PutEx</a> method, the document of which provides an example of how to use these enumerated constants.

Because Visual Basic Scripting Edition (VBScript) cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined. Use the numeric constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI
    Enumerations</a>



<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs.PutEx</a>
 

 

