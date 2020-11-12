---
UID: NS:cmdtree.tagDBCOMMANDTREE
title: DBCOMMANDTREE (cmdtree.h)
description: The DBCOMMANDTREE structure is the primary data structure used to represent any node in an OLE DB command tree, as described in the Data Manipulation Operators and Data Definition Operators section of this reference.
helpviewer_keywords: ["DBCOMMANDTREE","DBCOMMANDTREE structure [Indexing Service]","_idxs_DBCOMMANDTREE","cmdtree/","indexsrv.dbcommandtree","tagDBCOMMANDTREE"]
old-location: indexsrv\dbcommandtree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_29lx.htm
ms.date: 12/05/2018
ms.keywords: DBCOMMANDTREE, DBCOMMANDTREE structure [Indexing Service], _idxs_DBCOMMANDTREE, cmdtree/, indexsrv.dbcommandtree, tagDBCOMMANDTREE
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
req.typenames: DBCOMMANDTREE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDBCOMMANDTREE
 - cmdtree/tagDBCOMMANDTREE
 - DBCOMMANDTREE
 - cmdtree/DBCOMMANDTREE
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
 - DBCOMMANDTREE
---

# DBCOMMANDTREE structure


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBCOMMANDTREE</b> structure is the primary data structure used to represent any node in an OLE DB command tree, as described in the <a href="/previous-versions/windows/desktop/indexsrv/data-manipulation-operators">Data Manipulation Operators</a> and Data Definition Operators section of this reference. This structure is used for each data manipulation language (DML) or data definition language (DDL) node in an OLE DB command tree.

## -struct-fields

### -field op

Operator identifier (2 bytes)

A value of type <a href="/previous-versions/windows/desktop/indexsrv/dbcommandop">DBCOMMANDOP</a> from the <a href="/previous-versions/windows/desktop/api/cmdtree/ne-cmdtree-dbcommandopenum">DBCOMMANDOPENUM</a> enumeration. It specifies an operator from the <a href="/previous-versions/windows/desktop/indexsrv/data-manipulation-operators">Data Manipulation Operators</a> or the Data Definition Operators that defines the operation to take place on the associated field.

### -field wKind

Discriminator for the following union (2 bytes)

A value of type <a href="/previous-versions/windows/desktop/indexsrv/dbvaluekind">DBVALUEKIND</a> from the <a href="/previous-versions/windows/desktop/api/cmdtree/ne-cmdtree-dbvaluekindenum">DBVALUEKINDENUM</a> enumerated type. It defines the data type of the associated union member so that the command processor knows how to interpret it.

### -field pctFirstChild

Pointer to first child (4 bytes)

A pointer to the <b>DBCOMMANDTREE</b> structure that represents the first child of this node of the command tree.

### -field pctNextSibling

Pointer to sibling (4 bytes)

A pointer to the <b>DBCOMMANDTREE</b> structure that represents the next child of this node of the command tree.

### -field value

Union directly represents fields that fit within 8 bytes. Comments list DBVALUEKIND and DBTYPE corresponding to each field.

A union to hold the value for every data type supported by this OLE DB provider. For any union member data type that holds 8 bytes or less, the value itself is stored here. Otherwise, <b>llvalue</b> is a <b>pwszValue</b> member, a pointer to the data. 



A <b>pwszValue</b> member is a string; its interpretation is left to the provider. In other words, the consumer must understand the provider's method of name resolution. For command components "passed through" to another provider, it is left to the receiving provider to interpret the string.

The <b>pMoniker</b> member is used for unresolved linked objects, in particular tables and functions.

The <b>pRowset</b> member is used to reference a currently open rowset as input for a command. Most providers will fail if an <a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a> method is invoked while the command tree refers to an open rowset.

The <b>pCommand</b> member references another command object as input for a command. Most providers will fail if an <a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a> method is invoked while the command tree refers to a command object that does not support monikers.

### -field value.llValue

DBVALUEKIND_I8        (DBTYPE_I8)

### -field value.ullValue

DBVALUEKIND_UI8       (DBTYPE_UI8)

### -field value.fValue

DBVALUEKIND_BOOL      (DBTYPE_BOOL)

### -field value.uchValue

DBVALUEKIND_UI1       (DBTYPE_UI1)

### -field value.schValue

DBVALUEKIND_I1        (DBTYPE_I1)

### -field value.usValue

DBVALUEKIND_UI2       (DBTYPE_UI2)

### -field value.sValue

DBVALUEKIND_I2        (DBTYPE_I2)

### -field value.pwszValue

DBVALUEKIND_WSTR      (DBTYPE_WSTR)

### -field value.lValue

DBVALUEKIND_I4        (DBTYPE_I4)

### -field value.ulValue

DBVALUEKIND_UI4       (DBTYPE_UI4)

### -field value.flValue

DBVALUEKIND_R4        (DBTYPE_R4)

### -field value.dblValue

DBVALUEKIND_R8        (DBTYPE_R8)

### -field value.cyValue

DBVALUEKIND_CY        (DBTYPE_CY)

### -field value.dateValue

DBVALUEKIND_DATE      (DBTYPE_DATE)

### -field value.dbdateValue

DBVALUEKIND_DBDATE    (DBTYPE_DBDATE)

### -field value.dbtimeValue

DBVALUEKIND_DBTIME    (DBTYPE_DBTIME)

### -field value.scodeValue

DBVALUEKIND_ERROR     (DBTYPE_ERROR)

### -field value.pbstrValue

DBVALUEKIND_BSTR      (DBTYPE_BSTR)

### -field value.pCommand

DBVALUEKIND_COMMAND   (DBTYPE_IUNKNOWN)

### -field value.pDispatch

DBVALUEKIND_IDISPATCH (DBTYPE_IDISPATCH)

### -field value.pMoniker

DBVALUEKIND_MONIKER   (DBTYPE_MONIKER)

### -field value.pRowset

DBVALUEKIND_ROWSET    (DBTYPE_ROWSET)

### -field value.pUnknown

DBVALUEKIND_IUNKNOWN  (DBTYPE_IUNKNOWN)

### -field value.pdbbygdValue

DBVALUEKIND_BYGUID

### -field value.pcoldescValue

DBVALUEKIND_COLDESC

### -field value.pdbidValue

DBVALUEKIND_ID

### -field value.pdblikeValue

DBVALUEKIND_LIKE

### -field value.pdbcntntValue

DBVALUEKIND_CONTENT

### -field value.pdbcntntscpValue

DBVALUEKIND_CONTENTSCOPE

### -field value.pdbcntnttblValue

DBVALUEKIND_CONTENTTABLE

### -field value.pdbcntntvcValue

DBVALUEKIND_CONTENTVECTOR

### -field value.pdbcntntproxValue

DBVALUEKIND_CONTENTPROXIMITY

### -field value.pdbgrpinfValue

DBVALUEKIND_GROUPINFO

### -field value.pdbparamValue

DBVALUEKIND_PARAMETER

### -field value.pdbpropValue

DBVALUEKIND_PROPERTY

### -field value.pdbstfncValue

DBVALUEKIND_SETFUNC

### -field value.pdbsrtinfValue

DBVALUEKIND_SORTINFO

### -field value.pdbtxtValue

DBVALUEKIND_TEXT

### -field value.pdbvectorValue

DBVALUEKIND_VECTOR | *

### -field value.parrayValue

DBVALUEKIND_ARRAY | *

### -field value.pvarValue

DBVALUEKIND_VARIANT  (DBTYPE_VARIANT)

### -field value.pGuid

DBVALUEKIND_GUID     (DBTYPE_GUID)

### -field value.pbValue

DBVALUEKIND_BYTES    (DBTYPE_BYTES)

### -field value.pzValue

DBVALUEKIND_STR      (DBTYPE_STR)

### -field value.pdbnValue

DBVALUEKIND_NUMERIC  (DBTYPE_NUMERIC)

### -field value.pdbtsValue

DBVALUEKIND_DBTIMESTAMP (DBTYPE_DBTIMESTAMP)

### -field value.pvValue

a generic DBVALUEKIND_BYREF

### -field value.pdbprobValue

DBVALUEKIND_PROBABILISTIC

### -field value.pdbreldocValue

DBVALUEKIND_RELEVANTDOCUMENT

### -field hrError

Error indicator, details in Extended Error info (4 bytes)

## -remarks

Many operations create a binding environment. For example, a DBOP_select operation has two inputs — a table and a Boolean predicate. (For more information on this operation, see <a href="/previous-versions/windows/desktop/indexsrv/operators-with-two-variants-for-ordered-and-non-ordered-tables">Operators with Two Variants for Ordered and Non-Ordered Tables</a>.) By virtue of the "select" operation, the table becomes the binding environment for the predicate. That means that the predicate may freely reference column names defined in the table. Note that not all bindings must come from the nearest table operation. For example, there might be multiple table operations within an "exist" expression, and any predicate may reference a column defined outside the "exist" expression. (In SQL, this is called a "correlated subquery.")

The typical size of a <b>DBCOMMANDTREE</b> structure for a node is 24 bytes. However, operators may store some specific information in the value field of the node. For programming convenience, the union field includes branches representing some common types that can fit within 8 bytes. Variable-length types are referenced via a pointer to the corresponding structure (such as <a href="/previous-versions/windows/desktop/indexsrv/dbtext">DBTEXT</a>). The discriminator for the union is of type <b>WORD</b> rather than <a href="/previous-versions/windows/desktop/indexsrv/dbvaluekind">DBVALUEKIND</a> so that it is possible to store node values such as DBVALUEKIND_VECTOR | DBVALUEKIND_GUID, DBVALUEKIND_BYREF | DBVALUEKIND_UI4, or DBVALUEKIND_SAFEARRAY | DBVALUEKIND_I4.