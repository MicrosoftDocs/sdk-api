---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0027
title: "__MIDL___MIDL_itf_ads_0000_0000_0027"
author: windows-sdk-content
description: Specifies ways to update a named property in the cache.
old-location: adsi\ads_property_operation_enum.htm
tech.root: ADSI
ms.assetid: fba20292-870d-4948-abf1-225b1230e938
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ADS_PROPERTY_APPEND, ADS_PROPERTY_CLEAR, ADS_PROPERTY_DELETE, ADS_PROPERTY_OPERATION_ENUM, ADS_PROPERTY_OPERATION_ENUM enumeration [ADSI], ADS_PROPERTY_UPDATE, __MIDL___MIDL_itf_ads_0000_0000_0027, _ds_ads_property_operation_enum, adsi.ads__property__operation__enum, adsi.ads_property_operation_enum, iads/ADS_PROPERTY_APPEND, iads/ADS_PROPERTY_CLEAR, iads/ADS_PROPERTY_DELETE, iads/ADS_PROPERTY_OPERATION_ENUM, iads/ADS_PROPERTY_UPDATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_PROPERTY_OPERATION_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_PROPERTY_OPERATION_ENUM
req.redist: 
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
 

 

