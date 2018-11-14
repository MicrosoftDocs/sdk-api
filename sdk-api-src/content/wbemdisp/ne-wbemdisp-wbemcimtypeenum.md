---
UID: NE:wbemdisp.WbemCimtypeEnum
title: WbemCimtypeEnum
author: windows-sdk-content
description: Define the valid CIM types of a property value.
old-location: wmi\wbemcimtypeenum.htm
tech.root: WmiSdk
ms.assetid: d9929464-742e-4f6c-b631-a6c191167858
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: WbemCimTypeEnum, WbemCimTypeEnum enumeration [Windows Management Instrumentation], WbemCimtypeEnum, _hmm_wbemcimtypeenum, wbemCimtypeBoolean, wbemCimtypeChar16, wbemCimtypeDatetime, wbemCimtypeObject, wbemCimtypeReal32, wbemCimtypeReal64, wbemCimtypeReference, wbemCimtypeSint16, wbemCimtypeSint32, wbemCimtypeSint64, wbemCimtypeSint8, wbemCimtypeString, wbemCimtypeUint16, wbemCimtypeUint32, wbemCimtypeUint64, wbemCimtypeUint8, wbemdisp/WbemCimTypeEnum, wbemdisp/wbemCimtypeBoolean, wbemdisp/wbemCimtypeChar16, wbemdisp/wbemCimtypeDatetime, wbemdisp/wbemCimtypeObject, wbemdisp/wbemCimtypeReal32, wbemdisp/wbemCimtypeReal64, wbemdisp/wbemCimtypeReference, wbemdisp/wbemCimtypeSint16, wbemdisp/wbemCimtypeSint32, wbemdisp/wbemCimtypeSint64, wbemdisp/wbemCimtypeSint8, wbemdisp/wbemCimtypeString, wbemdisp/wbemCimtypeUint16, wbemdisp/wbemCimtypeUint32, wbemdisp/wbemCimtypeUint64, wbemdisp/wbemCimtypeUint8, wmi.wbemcimtypeenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
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
 - Wbemdisp.h
api_name:
 - WbemCimTypeEnum
product: Windows
targetos: Windows
req.typenames: WbemCimtypeEnum
req.redist: 
---

# WbemCimtypeEnum enumeration


## -description


The 
WbemCimtypeEnum constants define the valid CIM types of a property value.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use the Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemCimtypeSint8

Signed 8-bit integer


### -field wbemCimtypeUint8

Unsigned 8-bit integer


### -field wbemCimtypeSint16

Signed 16-bit integer


### -field wbemCimtypeUint16

Unsigned 16-bit integer


### -field wbemCimtypeSint32

Signed 32-bit integer


### -field wbemCimtypeUint32

Unsigned 32-bit integer


### -field wbemCimtypeSint64

Signed 64-bit integer


### -field wbemCimtypeUint64

Unsigned 64-bit integer


### -field wbemCimtypeReal32

32-bit real number


### -field wbemCimtypeReal64

64-bit real number


### -field wbemCimtypeBoolean

Boolean value


### -field wbemCimtypeString

String


### -field wbemCimtypeDatetime

Date/time value


### -field wbemCimtypeReference

Reference to a CIM object


### -field wbemCimtypeChar16

16-bit character


### -field wbemCimtypeObject

CIM object


## -see-also




<a href="https://msdn.microsoft.com/ab67954c-ead2-4906-9680-503612d3f12d">CIMTYPE_ENUMERATION</a>



<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 

