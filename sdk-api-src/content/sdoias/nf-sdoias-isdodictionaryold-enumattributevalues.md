---
UID: NF:sdoias.ISdoDictionaryOld.EnumAttributeValues
title: ISdoDictionaryOld::EnumAttributeValues
author: windows-sdk-content
description: The EnumAttributeValues method retrieves the values for an enumerable attribute.
old-location: nps\SDO_isdodictionaryold_enumattributevalues.htm
tech.root: Nps
ms.assetid: e46dc286-5316-49c2-a384-b486efc80d2a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumAttributeValues, EnumAttributeValues method [Network Policy Server], EnumAttributeValues method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],EnumAttributeValues method, ISdoDictionaryOld.EnumAttributeValues, ISdoDictionaryOld::EnumAttributeValues, _sdo_isdodictionaryold_enumattributevalues, nps.SDO_isdodictionaryold_enumattributevalues, sdo.isdodictionaryold_enumattributevalues, sdoias/ISdoDictionaryOld::EnumAttributeValues
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Iassdo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoDictionaryOld.EnumAttributeValues
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdoDictionaryOld::EnumAttributeValues


## -description


The 
<b>EnumAttributeValues</b> method retrieves the values for an enumerable attribute.


## -parameters




### -param Id [in]

Specifies the ID of the attribute.


### -param pValueIds [out]

On successful return points to a 
<a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> of value IDs for the enumerable attribute. If the attribute is not enumerable, points to a 
<a href="e305240e-9e11-4006-98cc-26f4932d2118">VT_EMPTY</a> variant.


### -param pValuesDesc [out]

On successful return points to a 
<a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> of value descriptions for the enumerable attribute. If the attribute is not enumerable, points to a 
<a href="e305240e-9e11-4006-98cc-26f4932d2118">VT_EMPTY</a> variant.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



The return value is S_OK even if the attribute is not enumerable.




## -see-also




<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>
 

 

