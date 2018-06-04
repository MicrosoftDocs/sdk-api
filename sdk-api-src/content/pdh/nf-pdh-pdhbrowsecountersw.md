---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PdhBrowseCountersW function


## -description


Displays a  <b>Browse Counters</b> dialog box that the user can use to select one or more counters that they want to add to the query.
			

To use handles to data sources, use the 
<a href="https://msdn.microsoft.com/ab835bf8-1adc-463f-99c3-654a328af98a">PdhBrowseCountersH</a> function.


## -parameters




### -param pBrowseDlgData [in]

A 
<a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a> structure that specifies the behavior of the dialog box.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>.




## -remarks



Note that the dialog
   box can return PDH_DIALOG_CANCELLED if <b>bSingleCounterPerDialog</b>
   is <b>FALSE</b> and the user clicks the  <b>Close</b> button, so your error handling would have to account for this.

For information on using this function, see <a href="https://msdn.microsoft.com/f2fac1d3-f643-43c9-a445-112015baecdd">Browsing Counters</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/44c5cfa8-6449-45d8-ac30-979b99c086de">Browsing Performance Counters</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b7a2112e-9f50-4a36-b022-f9609b2827bc">CounterPathCallBack</a>



<a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a>



<a href="https://msdn.microsoft.com/ab835bf8-1adc-463f-99c3-654a328af98a">PdhBrowseCountersH</a>
 

 

