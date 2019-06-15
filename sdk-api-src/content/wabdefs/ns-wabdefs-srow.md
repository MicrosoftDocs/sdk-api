---
UID: NS:wabdefs._SRow
title: SRow (wabdefs.h)
author: windows-sdk-content
description: Do not use. Describes a row from a table containing selected properties for a specific object.
old-location: wab\_wab_SRow.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\srow.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSRow, LPSRow, LPSRow structure pointer [Windows Address Book], SRow, SRow structure [Windows Address Book], _wab_SRow, wab._wab_SRow, wabdefs/LPSRow, wabdefs/SRow"
ms.topic: struct
f1_keywords: ["wabdefs/SRow"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SRow
product: Windows
targetos: Windows
req.typenames: SRow, *LPSRow
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# SRow structure


## -description


Do not use. Describes a row from a table containing selected properties for a specific object.


## -struct-fields




### -field ulAdrEntryPad

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of padding bytes for aligning properly the property values to which the <b>lpProps</b> member points.


### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the count of property values to which <b>lpProps</b> points.


### -field lpProps

Type: <b>LPSPropValue</b>

Pointer to an array of variables of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wabdefs/ns-wabdefs-_spropvalue">SPropValue</a> that describe the property values for the columns in the row.

