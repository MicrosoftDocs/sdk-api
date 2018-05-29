---
UID: NF:sdoias.ISdoDictionaryOld.EnumAttributes
title: ISdoDictionaryOld::EnumAttributes
author: windows-sdk-content
description: The EnumAttributes method retrieves the values of the specified attributes.
old-location: nps\SDO_isdodictionaryold_enumattributes.htm
old-project: Nps
ms.assetid: 45327428-1442-43f7-bf5b-0b6fcf06a246
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EnumAttributes, EnumAttributes method [Network Policy Server], EnumAttributes method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],EnumAttributes method, ISdoDictionaryOld.EnumAttributes, ISdoDictionaryOld::EnumAttributes, _sdo_isdodictionaryold_enumattributes, nps.SDO_isdodictionaryold_enumattributes, sdo.isdodictionaryold_enumattributes, sdoias/ISdoDictionaryOld::EnumAttributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VENDORPROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Iassdo.dll
api_name:
-	ISdoDictionaryOld.EnumAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISdoDictionaryOld::EnumAttributes


## -description


The 
<b>EnumAttributes</b> method retrieves the values of the specified attributes.


## -parameters




### -param Id [in, out]

On input, a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> 
       that specifies the attributes to enumerate. If the type of this 
       <b>VARIANT</b>, given by 
       <b>V_VT</b>(Id), is 
       <b>VT_EMPTY</b>, 
       <b>ISdoDictionaryOld::EnumAttributes</b> 
       enumerates all the attributes. If the type is <b>VT_I4</b>, then the value of the 
       <b>VARIANT</b> is the ID of the attribute 
       to enumerate.

On output, pointer to a 
       <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> that contains the IDs of 
       the enumerated attributes.


### -param pValues [out]

Pointer to a 
      <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> that contains 
      the values of the enumerated attributes.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



The parameters must not be <b>NULL</b>.

If VT(Id) = VT_EMPTY then all the attributes are returned. Otherwise VT(Id) should be <b>VT_I4</b> and only the attributes designed are retrieved.

When the method returns, Id is a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> of the Ids returned, and <i>pValues</i> is a <b>SAFEARRAY</b> of the values returned.




## -see-also




<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>
 

 

