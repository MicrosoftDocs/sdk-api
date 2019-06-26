---
UID: NE:propsys.PROPDESC_SEARCHINFO_FLAGS
title: PROPDESC_SEARCHINFO_FLAGS (propsys.h)
author: windows-sdk-content
description: Determines whether and how a property is indexed by Windows Search.
old-location: properties\PROPDESC_SEARCHINFO_FLAGS.htm
tech.root: properties
ms.assetid: 49e858e3-0231-45ce-a5a8-a1c4536577a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDSIF_ALWAYSINCLUDE, PDSIF_DEFAULT, PDSIF_ININVERTEDINDEX, PDSIF_ISCOLUMN, PDSIF_ISCOLUMNSPARSE, PDSIF_USEFORTYPEAHEAD, PROPDESC_SEARCHINFO_FLAGS, PROPDESC_SEARCHINFO_FLAGS enumeration [Windows Properties], _shell_PROPDESC_SEARCHINFO_FLAGS, properties.PROPDESC_SEARCHINFO_FLAGS, propsys/PDSIF_ALWAYSINCLUDE, propsys/PDSIF_DEFAULT, propsys/PDSIF_ININVERTEDINDEX, propsys/PDSIF_ISCOLUMN, propsys/PDSIF_ISCOLUMNSPARSE, propsys/PDSIF_USEFORTYPEAHEAD, propsys/PROPDESC_SEARCHINFO_FLAGS, shell.PROPDESC_SEARCHINFO_FLAGS
ms.topic: enum
f1_keywords: 
 - "propsys/PROPDESC_SEARCHINFO_FLAGS"
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - PROPDESC_SEARCHINFO_FLAGS
product: Windows
targetos: Windows
req.typenames: PROPDESC_SEARCHINFO_FLAGS
req.redist: 
ms.custom: 19H1
---

# PROPDESC_SEARCHINFO_FLAGS enumeration


## -description


Determines whether and how a property is indexed by Windows Search.


## -enum-fields




### -field PDSIF_DEFAULT

The property is not indexed.


### -field PDSIF_ININVERTEDINDEX

The property is in an inverted index to help speed searches.


### -field PDSIF_ISCOLUMN

The property is indexed by Windows Search.


### -field PDSIF_ISCOLUMNSPARSE

The property is indexed to save space for properties that are not present on all files.


### -field PDSIF_ALWAYSINCLUDE

<b>Windows 7 and later</b>. The property mnemonics are recognized by AQS even if the property is not a column (PDSIF_ISCOLUMN).


### -field PDSIF_USEFORTYPEAHEAD

Check this property for matches when looking for type ahead results.  


## -remarks



For third parties, the PDSIF_ALWAYSINCLUDE flag can be referred to in user-specified query strings, even though its value may not be retrievable from the index in query results. The meaning of the PDSIF_ALWAYSINCLUDE flag to the indexer when a third party sets the flag through a custom schema definition is that it enables users to refer to this property in query strings even though its value is not stored in the index.

Property mnemonics refers to a shortened name for a property. 



