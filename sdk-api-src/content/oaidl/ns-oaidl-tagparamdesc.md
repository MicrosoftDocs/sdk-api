---
UID: NS:oaidl.tagPARAMDESC
title: tagPARAMDESC
author: windows-sdk-content
description: Contains information needed for transferring a structure element, parameter, or function return value between processes.
old-location: automat\paramdesc.htm
old-project: automat
ms.assetid: 3b3b2c54-1997-4d1f-9934-81621500b2b9
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: "*LPPARAMDESC, LPPARAMDESC, LPPARAMDESC structure pointer [Automation], PARAMDESC, PARAMDESC structure [Automation], _oa96_PARAMDESC, automat.paramdesc, oaidl/LPPARAMDESC, oaidl/PARAMDESC, tagPARAMDESC"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PARAMDESC, *LPPARAMDESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - PARAMDESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagPARAMDESC structure


## -description


Contains information needed for transferring a structure element, parameter, or function return value between processes.


## -struct-fields




### -field pparamdescex

The default value for the parameter, if PARAMFLAG_FHASDEFAULT is specified in <b>wParamFlags</b>.


### -field wParamFlags

The parameter flags. See <a href="https://msdn.microsoft.com/0273322a-1ba6-48eb-8eb7-f273f5240bdd">PARAMFLAG Constants</a>.

