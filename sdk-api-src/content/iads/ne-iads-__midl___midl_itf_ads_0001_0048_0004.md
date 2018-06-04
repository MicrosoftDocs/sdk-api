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

# __MIDL___MIDL_itf_ads_0001_0048_0004 enumeration


## -description


The <b>ADS_FLAGTYPE_ENUM</b> enumeration specifies values that can be used to indicate the presence of the <b>ObjectType</b> or <b>InheritedObjectType</b> fields in the access-control entry (ACE).


## -enum-fields




### -field ADS_FLAG_OBJECT_TYPE_PRESENT

The <b>ObjectType</b> field is present in the ACE.


### -field ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT

The <b>InheritedObjectType</b> field is present in the ACE.


## -remarks



<b>ObjectType</b> indicates what object type, property set, or property an ACE refers to. It takes a GUID as its value. The GUID referenced by <b>ObjectType</b> is not physically present in the ACE unless ADS_FLAGS_OBJECT_TYPE_PRESENT is set.

<b>InheritedObjectType</b> specifies the GUID of an object that will inherit the ACE. The GUID is not physically present in the ACE unless the ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT bit is set.

<div class="alert"><b>Note</b>  Because VBScript cannot read information from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>
 

 

