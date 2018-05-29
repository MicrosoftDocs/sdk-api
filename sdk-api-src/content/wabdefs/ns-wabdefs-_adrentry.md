---
UID: NS:wabdefs._ADRENTRY
title: "_ADRENTRY"
author: windows-sdk-content
description: Do not use. Describes zero or more properties belonging to one or more recipients.
old-location: wab\_wab_ADRENTRY.htm
old-project: wab
ms.assetid: VS|wab|~\wab\reference\structures\adrentry.htm
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPADRENTRY, ADRENTRY, ADRENTRY structure [Windows Address Book], Gender, Gender structure [Windows Address Book], _ADRENTRY, _wab_ADRENTRY, wab._wab_ADRENTRY, wabdefs/ADRENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: ADRENTRY, *LPADRENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wabdefs.h
api_name:
-	Gender
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# _ADRENTRY structure


## -description


Do not use. Describes zero or more properties belonging to one or more recipients.


## -struct-fields




### -field ulReserved1

Type: <b>ULONG</b>


### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the count of properties in the property value array to which the <b>rgPropVals</b> member points. The <b>cValues</b> member can be zero.


### -field rgPropVals

Type: <b>LPSPropValue</b>

Pointer to a variable of type <a href="https://msdn.microsoft.com/cff1b41d-fc53-4987-8823-04cbd51e811b">SPropValue</a> that specifies the property value array describing the properties for the recipient. The <b>rgPropVals</b> member can be <b>NULL</b>.

