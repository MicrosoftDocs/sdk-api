---
UID: NF:bdaiface.IBDA_ConditionalAccess.get_SmartCardInfo
title: IBDA_ConditionalAccess::get_SmartCardInfo (bdaiface.h)
description: The get_SmartCardInfo method retrieves information about the smart card.
helpviewer_keywords: ["IBDA_ConditionalAccess interface [Microsoft TV Technologies]","get_SmartCardInfo method","IBDA_ConditionalAccess.get_SmartCardInfo","IBDA_ConditionalAccess::get_SmartCardInfo","IBDA_ConditionalAccessget_SmartCardInfo","bdaiface/IBDA_ConditionalAccess::get_SmartCardInfo","get_SmartCardInfo","get_SmartCardInfo method [Microsoft TV Technologies]","get_SmartCardInfo method [Microsoft TV Technologies]","IBDA_ConditionalAccess interface","mstv.ibda_conditionalaccess_get_smartcardinfo"]
old-location: mstv\ibda_conditionalaccess_get_smartcardinfo.htm
tech.root: mstv
ms.assetid: 0c9143e7-1e59-4f64-84b8-2bbac18cf787
ms.date: 12/05/2018
ms.keywords: IBDA_ConditionalAccess interface [Microsoft TV Technologies],get_SmartCardInfo method, IBDA_ConditionalAccess.get_SmartCardInfo, IBDA_ConditionalAccess::get_SmartCardInfo, IBDA_ConditionalAccessget_SmartCardInfo, bdaiface/IBDA_ConditionalAccess::get_SmartCardInfo, get_SmartCardInfo, get_SmartCardInfo method [Microsoft TV Technologies], get_SmartCardInfo method [Microsoft TV Technologies],IBDA_ConditionalAccess interface, mstv.ibda_conditionalaccess_get_smartcardinfo
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - IBDA_ConditionalAccess::get_SmartCardInfo
 - bdaiface/IBDA_ConditionalAccess::get_SmartCardInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_ConditionalAccess.get_SmartCardInfo
---

# IBDA_ConditionalAccess::get_SmartCardInfo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SmartCardInfo</b> method retrieves information about the smart card.

## -parameters

### -param pbstrCardName [out]

Receives a string containing the card name. When the string is no longer required, call the <b>SysFreeString</b> function to free it.

### -param pbstrCardManufacturer [out]

Receives a string containing the name of the card manufacturer. When the string is no longer required, call the <b>SysFreeString</b> function to free it.

### -param pfDaylightSavings [out]

Receives a value indicating whether daylight savings is in effect. If the value is VARIANT_TRUE, daylight savings is in effect. If the value is VARIANT_FALSE, daylight savings is not in effect.

### -param pbyRatingRegion [out]

Receives a value indicating the rating region.

### -param plTimeZoneOffsetMinutes [out]

Receives the time zone offset in minutes.

### -param pbstrLanguage [out]

Receives a string indicating the language. When the string is no longer required, call the <b>SysFreeString</b> function to free it.

### -param pEALocationCode [out]

Pointer to a buffer that receives the emergency alert location code information. The buffer size must be at least <code>sizeof(EALocationCodeType)</code>. The method writes a structure of type <a href="/windows/desktop/api/bdaiface/ns-bdaiface-ealocationcodetype">EALocationCodeType</a> to the buffer. The structure specifies the location code scheme (for example, SCTE 18), state, county, and county subdivision for the emergency alert.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_conditionalaccess">IBDA_ConditionalAccess Interface</a>