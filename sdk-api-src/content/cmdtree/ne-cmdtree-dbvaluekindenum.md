---
UID: NE:cmdtree.DBVALUEKINDENUM
title: DBVALUEKINDENUM (cmdtree.h)
description: The DBVALUEKINDENUM enumerated type is used to indicate the type of the union member inside a DBCOMMANDTREE structure.
helpviewer_keywords: ["DBVALUEKINDENUM","DBVALUEKINDENUM enumeration [Indexing Service]","See below.","_idxs_DBVALUEKINDENUM","cmdtree/DBVALUEKINDENUM","cmdtree/See below.","indexsrv.dbvaluekindenum"]
old-location: indexsrv\dbvaluekindenum.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_8565.htm
ms.date: 12/05/2018
ms.keywords: DBVALUEKINDENUM, DBVALUEKINDENUM enumeration [Indexing Service], See below., _idxs_DBVALUEKINDENUM, cmdtree/DBVALUEKINDENUM, cmdtree/See below., indexsrv.dbvaluekindenum
req.header: cmdtree.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DBVALUEKINDENUM
 - cmdtree/DBVALUEKINDENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cmdtree.h
api_name:
 - DBVALUEKINDENUM
---

# DBVALUEKINDENUM enumeration


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBVALUEKINDENUM</b> enumerated type is used to indicate the type of the union member inside a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure. For programming convenience, the values in this enumeration correspond exactly to the OLE Automation <b>VARENUM</b> and OLE DB <b>DBTYPE</b> enumerations. The comments associated with each enumeration value represent the type and branch of the union type inside the command structure containing the value. nodes that do not assign a value to the union member should assign a DBVALUEKIND_EMPTY to the <b>wKind</b> member of the <b>DBCOMMANDTREE</b> structure.

## -enum-fields

### -field DBVALUEKIND_BYGUID:256

### -field DBVALUEKIND_COLDESC

### -field DBVALUEKIND_ID

### -field DBVALUEKIND_CONTENT

### -field DBVALUEKIND_CONTENTVECTOR

### -field DBVALUEKIND_GROUPINFO

### -field DBVALUEKIND_PARAMETER

### -field DBVALUEKIND_PROPERTY

### -field DBVALUEKIND_SETFUNC

### -field DBVALUEKIND_SORTINFO

### -field DBVALUEKIND_TEXT

### -field DBVALUEKIND_COMMAND

### -field DBVALUEKIND_MONIKER

### -field DBVALUEKIND_ROWSET

### -field DBVALUEKIND_LIKE

### -field DBVALUEKIND_CONTENTPROXIMITY

### -field DBVALUEKIND_CONTENTSCOPE

### -field DBVALUEKIND_CONTENTTABLE

### -field DBVALUEKIND_IDISPATCH:9

### -field DBVALUEKIND_IUNKNOWN:13

### -field DBVALUEKIND_EMPTY:0

### -field DBVALUEKIND_NULL:1

### -field DBVALUEKIND_I2:2

### -field DBVALUEKIND_I4:3

### -field DBVALUEKIND_R4:4

### -field DBVALUEKIND_R8:5

### -field DBVALUEKIND_CY:6

### -field DBVALUEKIND_DATE:7

### -field DBVALUEKIND_BSTR:8

### -field DBVALUEKIND_ERROR:10

### -field DBVALUEKIND_BOOL:11

### -field DBVALUEKIND_VARIANT:12

### -field DBVALUEKIND_VECTOR:0x1000

### -field DBVALUEKIND_ARRAY:0x2000

### -field DBVALUEKIND_BYREF:0x4000

### -field DBVALUEKIND_I1:16

### -field DBVALUEKIND_UI1:17

### -field DBVALUEKIND_UI2:18

### -field DBVALUEKIND_UI4

### -field DBVALUEKIND_I8

### -field DBVALUEKIND_UI8

### -field DBVALUEKIND_GUID:72

### -field DBVALUEKIND_BYTES:128

### -field DBVALUEKIND_STR:129

### -field DBVALUEKIND_WSTR:130

### -field DBVALUEKIND_NUMERIC:131

### -field DBVALUEKIND_DBDATE:133

### -field DBVALUEKIND_DBTIME:134

### -field DBVALUEKIND_DBTIMESTAMP:135

### -field DBVALUEKIND_PROBABILISTIC:136

### -field DBVALUEKIND_RELEVANTDOCUMENT:137

##### - See below.
