---
UID: NS:elscore._MAPPING_DATA_RANGE
title: "_MAPPING_DATA_RANGE"
author: windows-sdk-content
description: Contains text recognition results for a recognized text subrange. An array of structures of this type is retrieved by an Extended Linguistic Services (ELS) service in a MAPPING_PROPERTY_BAG structure.
old-location: intl\mappingdatarange.htm
old-project: Intl
ms.assetid: adff7901-1903-45dd-888f-1b8c5bb05de1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMAPPING_DATA_RANGE, MAPPING_DATA_RANGE, MAPPING_DATA_RANGE structure [Internationalization for Windows Applications], PMAPPING_DATA_RANGE, PMAPPING_DATA_RANGE structure pointer [Internationalization for Windows Applications], _MAPPING_DATA_RANGE, elscore/MAPPING_DATA_RANGE, elscore/PMAPPING_DATA_RANGE, intl.mappingdatarange"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: elscore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MAPPING_DATA_RANGE, *PMAPPING_DATA_RANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Elscore.h
api_name:
 - MAPPING_DATA_RANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _MAPPING_DATA_RANGE structure


## -description



Contains text recognition results for a recognized text subrange. An array of structures of this type is retrieved by an Extended Linguistic Services (ELS) service in a <a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a> structure.




## -struct-fields




### -field dwStartIndex

Index of the beginning of the subrange in the text, where 0 indicates the character at the pointer passed to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>, instead of an offset to the index passed to the function in the <i>dwIndex</i> parameter. The value should be less than the entire length of the text.


### -field dwEndIndex

Index of the end of the subrange in the text, where 0 indicates the character at the pointer passed to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>, instead of an offset to the index passed to the function in the <i>dwIndex</i> parameter. The value should be less than the entire length of the text.


### -field pszDescription

Reserved.


### -field dwDescriptionLength

Reserved.


### -field pData

Pointer to data retrieved as service output associated with the subrange. This data must be of the format indicated by the content type supplied in the <b>pszContentType</b> member. 


### -field dwDataSize

Size, in bytes, of the data specified in <b>pData</b>. Each service is required to report its output data size in bytes.


### -field pszContentType

Optional. Pointer to a string specifying the MIME content type of the data indicated by <b>pData</b>. Examples of content types are "text/plain", "text/html", and "text/css". 

<div class="alert"><b>Note</b>  In Windows 7, the ELS services support only the content type "text/plain". A content type specification can be found at <a href="http://go.microsoft.com/fwlink/p/?linkid=161570">Text Media Types</a>.</div>
<div> </div>

### -field prgActionIds

Available action Ids for this subrange. They are usable for calling <a href="https://msdn.microsoft.com/c3903d10-3429-4707-82b5-33efa6b2dc4c">MappingDoAction</a>.

<div class="alert"><b>Note</b>  In Windows 7, the ELS services do not expose any actions.</div>
<div> </div>

### -field dwActionsCount

The number of available actions for this subrange.

<div class="alert"><b>Note</b>  In Windows 7, the ELS services do not expose any actions.</div>
<div> </div>

### -field prgActionDisplayNames

Action display names for this subrange. These strings can be localized.

<div class="alert"><b>Note</b>  In Windows 7, the ELS services do not expose any actions.</div>
<div> </div>

## -remarks



<div class="alert"><b>Note</b>  The application should not alter any of the members of this data structure.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/58cdccf8-f052-4bb3-9391-2cc537d820dd">Extended Linguistic Services Structures</a>



<a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a>
 

 

