---
UID: NF:tspi.TSPI_phoneGetDisplay
title: TSPI_phoneGetDisplay function
author: windows-sdk-content
description: The TSPI_phoneGetDisplay function returns the current contents of the specified phone display.
old-location: tspi\tspi_phonegetdisplay.htm
old-project: tapi
ms.assetid: dff5fdc5-a627-4282-85d3-2a7ceaf063ed
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_phoneGetDisplay, TSPI_phoneGetDisplay function [TAPI 2.2], _tspi_tspi_phonegetdisplay, tspi.tspi_phonegetdisplay, tspi/TSPI_phoneGetDisplay
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tspi.h
req.include-header: 
req.redist: 
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
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneGetDisplay
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_phoneGetDisplay function


## -description


The 
<b>TSPI_phoneGetDisplay</b> function returns the current contents of the specified phone display.


## -parameters




### -param hdPhone

The handle to the phone to be queried.


### -param lpDisplay

A pointer to the memory location where the display content is to be stored by the provider, of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>. Prior to calling 
<b>TSPI_phoneGetDisplay</b>, the application sets the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.




## -remarks



The <i>lpDisplay</i> memory area should be at least <b>dwDisplayNumRows</b> * <b>dwDisplayNumColumns</b> elements in size to receive all of the display information. The <b>dwDisplayNumRows</b> and <b>dwDisplayNumColumns</b> members are available in the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure returned by 
<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>.

The service provider fills in all the members of the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/c320122c-037a-40f5-8314-6aa3352cc994">TSPI_phoneSetDisplay</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>
 

 

