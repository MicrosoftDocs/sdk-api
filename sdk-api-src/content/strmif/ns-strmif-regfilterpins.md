---
UID: NS:strmif.REGFILTERPINS
title: REGFILTERPINS
author: windows-sdk-content
description: The REGFILTERPINS structure contains pin information for registering a filter.
old-location: dshow\regfilterpins.htm
old-project: DirectShow
ms.assetid: 1da033e1-24c3-46e0-becf-025966e6238f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: AMOVIESETUP_PIN, AMOVIESETUP_PIN structure [DirectShow], LPAMOVIESETUP_PIN, LPAMOVIESETUP_PIN structure pointer [DirectShow], PAMOVIESETUP_PIN, PAMOVIESETUP_PIN structure pointer [DirectShow], REGFILTERPINS, REGFILTERPINS structure [DirectShow], REGFILTERPINSStructure, dshow.regfilterpins, strmif/AMOVIESETUP_PIN, strmif/LPAMOVIESETUP_PIN, strmif/PAMOVIESETUP_PIN, strmif/REGFILTERPINS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: REGFILTERPINS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	REGFILTERPINS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# REGFILTERPINS structure


## -description



The <code>REGFILTERPINS</code> structure contains pin information for registering a filter.




## -struct-fields




### -field strName

Name of the pin. (Obsolete.)


### -field bRendered

If <b>TRUE</b>, the filter renders the input from this pin. (Applies only to input pins. For output pins, the value is always <b>FALSE</b>.)


### -field bOutput

If <b>TRUE</b>, this pin is an output pin. Otherwise, the pin is an input pin.


### -field bZero

If <b>TRUE</b>, the filter can have zero instances of this pin.


### -field bMany

If <b>TRUE</b>, the filter can create more than one instance of this type of pin.


### -field clsConnectsToFilter

Class identifier (CLSID) of the filter to which this pin connects. (Obsolete.)


### -field strConnectsToPin

Name of the pin to which this pin connects. (Obsolete.)


### -field nMediaTypes

Number of media types supported by this pin.


### -field lpMediaType

Pointer to an array of <a href="https://msdn.microsoft.com/aa31f856-4151-420d-a69d-34ef3a105130">REGPINTYPES</a> structures, of size <b>nMediaTypes</b>.


## -remarks



This structure is used in the <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> interface for filter registration. If you use this structure, set the <b>dwVersion</b> member of the <a href="https://msdn.microsoft.com/651b94e6-b343-4957-9781-768b04c098dd">REGFILTER2</a> structure to 1. If you need to register a medium or pin category for the pin, use the <a href="https://msdn.microsoft.com/a78327f1-a0aa-4e25-b6f8-cf45b92191fa">REGFILTERPINS2</a> structure instead. In that case, set the <b>REGFILTER2</b> structure's <b>dwVersion</b> member to 2.

The equivalent <b>AMOVIESETUP_PIN</b> type is used in class factory templates (<a href="https://msdn.microsoft.com/3dbe6402-15f8-4490-9fe2-bebaa4e79170">CFactoryTemplate</a>).

The <b>strName</b>, <b>clsConnectsToFilter</b>, and <b>strConnectsToPin</b> members are obsolete. Their values are not added to the registry.

For more information, see <a href="https://msdn.microsoft.com/2b6304c0-4b67-4723-94a0-7b1fff534f91">How to Register DirectShow Filters</a>.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

