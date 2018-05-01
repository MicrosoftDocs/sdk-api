---
UID: NN:wia_lh.IWiaErrorHandler
title: IWiaErrorHandler
author: windows-driver-content
description: The IWiaErrorHandler interface provides the GetStatusDescription and ReportStatus methods, which enable minidrivers to give users information about status or errors during a data transfer and possibly give an opportunity to recover from errors.
old-location: image\iwiaerrorhandler_interface.htm
old-project: image
ms.assetid: b441fbca-75fe-4b9d-a9d5-2ad5a4a55801
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaErrorHandler, IWiaErrorHandler interface [Imaging Devices], IWiaErrorHandler interface [Imaging Devices], described, IWiaErrorHandler_0a501695-14b7-4aab-aee8-19ce74caea94.xml, image.iwiaerrorhandler_interface, wia_lh/IWiaErrorHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wia_lh.h
req.include-header: 
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wia_lh.h
api_name:
-	IWiaErrorHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaErrorHandler interface


## -description


The <b>IWiaErrorHandler</b> interface provides the <a href="https://msdn.microsoft.com/c3b5622d-9d51-4008-abb0-c8a60c4a6b16">GetStatusDescription</a> and <a href="https://msdn.microsoft.com/c244d5a1-d3c1-4f8f-9b55-3729e5f13887">ReportStatus</a> methods, which enable minidrivers to give users information about status or errors during a data transfer and possibly give an opportunity to recover from errors.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaErrorHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaErrorHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaErrorHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3b5622d-9d51-4008-abb0-c8a60c4a6b16">GetStatusDescription</a>
</td>
<td align="left" width="63%">
 The system UI calls the <a href="https://msdn.microsoft.com/c3b5622d-9d51-4008-abb0-c8a60c4a6b16">GetStatusDescription</a> method to provide the user with extra information about an error, if the user requests this information. This method is implemented by a driver's UI extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543909">IWiaErrorHandler::ReportStatus</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c244d5a1-d3c1-4f8f-9b55-3729e5f13887">ReportStatus</a> method displays information about an error or status during a transfer. In some cases this method allows the user to recover from an error.

</td>
</tr>
</table> 

