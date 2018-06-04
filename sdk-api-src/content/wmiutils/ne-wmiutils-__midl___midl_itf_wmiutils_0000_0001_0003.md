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

# __MIDL___MIDL_itf_wmiutils_0000_0001_0003 enumeration


## -description


Contains flags that indicate the features in a query.


## -enum-fields




### -field WMIQ_ASSOCQ_ASSOCIATORS

Associators exist in the query.


### -field WMIQ_ASSOCQ_REFERENCES

References exist in the query.


### -field WMIQ_ASSOCQ_RESULTCLASS

A result class is specified in the query.


### -field WMIQ_ASSOCQ_ASSOCCLASS

An association class is specified in the query.


### -field WMIQ_ASSOCQ_ROLE

A role is specified in the query.


### -field WMIQ_ASSOCQ_RESULTROLE

A result role is specified in the query.


### -field WMIQ_ASSOCQ_REQUIREDQUALIFIER

Required qualifiers are specified in the query.


### -field WMIQ_ASSOCQ_REQUIREDASSOCQUALIFIER

Required association qualifiers are specified in the query.


### -field WMIQ_ASSOCQ_CLASSDEFSONLY

The query specifies class definitions only.


### -field WMIQ_ASSOCQ_KEYSONLY

The query contains the <b>KEYSONLY</b> keyword.


### -field WMIQ_ASSOCQ_SCHEMAONLY

The query returns only the schema.


### -field WMIQ_ASSOCQ_CLASSREFSONLY

The query returns only the class references.

