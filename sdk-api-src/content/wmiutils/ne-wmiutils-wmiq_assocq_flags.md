---
UID: NE:wmiutils.__MIDL___MIDL_itf_wmiutils_0000_0001_0003
title: WMIQ_ASSOCQ_FLAGS (wmiutils.h)
description: Contains flags that indicate the features in a query.helpviewer_keywords: ["WMIQ_ASSOCQ_ASSOCCLASS","WMIQ_ASSOCQ_ASSOCIATORS","WMIQ_ASSOCQ_CLASSDEFSONLY","WMIQ_ASSOCQ_CLASSREFSONLY","WMIQ_ASSOCQ_FLAGS","WMIQ_ASSOCQ_FLAGS enumeration [Windows Management Instrumentation]","WMIQ_ASSOCQ_KEYSONLY","WMIQ_ASSOCQ_REFERENCES","WMIQ_ASSOCQ_REQUIREDASSOCQUALIFIER","WMIQ_ASSOCQ_REQUIREDQUALIFIER","WMIQ_ASSOCQ_RESULTCLASS","WMIQ_ASSOCQ_RESULTROLE","WMIQ_ASSOCQ_ROLE","WMIQ_ASSOCQ_SCHEMAONLY","wmi.wmiq_assocq_flags","wmiutils/WMIQ_ASSOCQ_ASSOCCLASS","wmiutils/WMIQ_ASSOCQ_ASSOCIATORS","wmiutils/WMIQ_ASSOCQ_CLASSDEFSONLY","wmiutils/WMIQ_ASSOCQ_CLASSREFSONLY","wmiutils/WMIQ_ASSOCQ_FLAGS","wmiutils/WMIQ_ASSOCQ_KEYSONLY","wmiutils/WMIQ_ASSOCQ_REFERENCES","wmiutils/WMIQ_ASSOCQ_REQUIREDASSOCQUALIFIER","wmiutils/WMIQ_ASSOCQ_REQUIREDQUALIFIER","wmiutils/WMIQ_ASSOCQ_RESULTCLASS","wmiutils/WMIQ_ASSOCQ_RESULTROLE","wmiutils/WMIQ_ASSOCQ_ROLE","wmiutils/WMIQ_ASSOCQ_SCHEMAONLY"]
old-location: wmi\wmiq_assocq_flags.htm
tech.root: WmiSdk
ms.assetid: bc436326-c763-448d-8757-38917e13a73f
ms.date: 12/05/2018
ms.keywords: WMIQ_ASSOCQ_ASSOCCLASS, WMIQ_ASSOCQ_ASSOCIATORS, WMIQ_ASSOCQ_CLASSDEFSONLY, WMIQ_ASSOCQ_CLASSREFSONLY, WMIQ_ASSOCQ_FLAGS, WMIQ_ASSOCQ_FLAGS enumeration [Windows Management Instrumentation], WMIQ_ASSOCQ_KEYSONLY, WMIQ_ASSOCQ_REFERENCES, WMIQ_ASSOCQ_REQUIREDASSOCQUALIFIER, WMIQ_ASSOCQ_REQUIREDQUALIFIER, WMIQ_ASSOCQ_RESULTCLASS, WMIQ_ASSOCQ_RESULTROLE, WMIQ_ASSOCQ_ROLE, WMIQ_ASSOCQ_SCHEMAONLY, wmi.wmiq_assocq_flags, wmiutils/WMIQ_ASSOCQ_ASSOCCLASS, wmiutils/WMIQ_ASSOCQ_ASSOCIATORS, wmiutils/WMIQ_ASSOCQ_CLASSDEFSONLY, wmiutils/WMIQ_ASSOCQ_CLASSREFSONLY, wmiutils/WMIQ_ASSOCQ_FLAGS, wmiutils/WMIQ_ASSOCQ_KEYSONLY, wmiutils/WMIQ_ASSOCQ_REFERENCES, wmiutils/WMIQ_ASSOCQ_REQUIREDASSOCQUALIFIER, wmiutils/WMIQ_ASSOCQ_REQUIREDQUALIFIER, wmiutils/WMIQ_ASSOCQ_RESULTCLASS, wmiutils/WMIQ_ASSOCQ_RESULTROLE, wmiutils/WMIQ_ASSOCQ_ROLE, wmiutils/WMIQ_ASSOCQ_SCHEMAONLY
f1_keywords:
- wmiutils/WMIQ_ASSOCQ_FLAGS
dev_langs:
- c++
req.header: wmiutils.h
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
- WMIUtils.h
api_name:
- WMIQ_ASSOCQ_FLAGS
targetos: Windows
req.typenames: WMIQ_ASSOCQ_FLAGS
req.redist: 
ms.custom: 19H1
---

# WMIQ_ASSOCQ_FLAGS enumeration


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

