---
UID: NS:wabdefs._SRestriction
title: SRestriction (wabdefs.h)
description: Do not use. Describes a filter for limiting the view of a table to particular rows.
helpviewer_keywords: ["*LPSRestriction","RES_AND","RES_BITMASK","RES_COMMENT","RES_COMPAREPROPS","RES_CONTENT","RES_EXIST","RES_NOT","RES_OR","RES_PROPERTY","RES_SIZE","RES_SUBRESTRICTION","SRestriction","SRestriction structure [Windows Address Book]","_wab_SRestriction","wab._wab_SRestriction","wabdefs/SRestriction"]
old-location: wab\_wab_SRestriction.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\srestriction.htm
ms.date: 12/05/2018
ms.keywords: '*LPSRestriction, RES_AND, RES_BITMASK, RES_COMMENT, RES_COMPAREPROPS, RES_CONTENT, RES_EXIST, RES_NOT, RES_OR, RES_PROPERTY, RES_SIZE, RES_SUBRESTRICTION, SRestriction, SRestriction structure [Windows Address Book], _wab_SRestriction, wab._wab_SRestriction, wabdefs/SRestriction'
req.header: wabdefs.h
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
req.typenames: '*LPSRestriction, SRestriction'
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _SRestriction
 - wabdefs/_SRestriction
 - LPSRestriction
 - wabdefs/LPSRestriction
 - SRestriction
 - wabdefs/SRestriction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SRestriction
---

# SRestriction structure


## -description

Do not use. Describes a filter for limiting the view of a table to particular rows.

## -struct-fields

### -field rt

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the restriction type. The possible values are as follows.



#### RES_AND

<b>SRestriction</b> structure describes an AND restriction, which applies a bitwise AND operation to a restriction.



#### RES_BITMASK

<b>SRestriction</b> structure describes a bitmask restriction, which applies a bitmask to a property value.



#### RES_COMMENT

<b>SRestriction</b> structure describes a comment restriction, which associates a comment with a restriction.



#### RES_COMPAREPROPS

<b>SRestriction</b> structure describes a compare properties restriction, which compares two property values. 



#### RES_CONTENT

<b>SRestriction</b> structure describes a content restriction, which searches a property value for specific content. 



#### RES_EXIST

<b>SRestriction</b> structure describes an exist restriction, which determines if a property is supported.



#### RES_NOT

<b>SRestriction</b> structure describes a NOT restriction, which applies a logical NOT operation to a restriction.



#### RES_OR

<b>SRestriction</b> structure describes an OR restriction, which applies a logical OR operation to a restriction.



#### RES_PROPERTY

<b>SRestriction</b> structure describes a property restriction, which determines if a property value matches a particular value.



#### RES_SIZE

<b>SRestriction</b> structure describes a size restriction, which determines if a property value is a particular size.



#### RES_SUBRESTRICTION

<b>SRestriction</b> structure describes a subobject restriction, which applies a restriction to a message's attachments or recipients.

### -field res

Union of restriction structures describing the filter to be applied. The specific structure included in the <b>res</b> member depends on the value of the <b>rt</b> member. The following list gives the mapping between the structure and the restriction type.

### -field res.resCompareProps

<b>Type: <b>SComparePropsRestriction</b>
</b>
RES_COMPAREPROPS

### -field res.resAnd

<b>Type: <b>SAndRestriction</b>
</b>
RES_AND

### -field res.resOr

<b>Type: <b>SOrRestriction</b>
</b>
RES_OR

### -field res.resNot

<b>Type: <b>SNotRestriction</b>
</b>
RES_NOT

### -field res.resContent

<b>Type: <b>SContentRestriction</b>
</b>
RES_CONTENT

### -field res.resProperty

<b>Type: <b>SPropertyRestriction</b>
</b>
RES_PROPERTY

### -field res.resBitMask

<b>Type: <b>SBitMaskRestriction</b>
</b>
RES_BITMASK

### -field res.resSize

<b>Type: <b>SSizeRestriction</b>
</b>
RES_SIZE

### -field res.resExist

<b>Type: <b>SExistRestriction</b>
</b>
RES_EXIST

### -field res.resSub

<b>Type: <b>SSubRestriction</b>
</b>
RES_SUBRESTRICTION

### -field res.resComment

<b>Type: <b>SCommentRestriction</b>
</b>
RES_COMMENT

