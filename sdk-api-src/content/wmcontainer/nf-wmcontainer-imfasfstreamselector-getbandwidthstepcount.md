---
UID: NF:wmcontainer.IMFASFStreamSelector.GetBandwidthStepCount
title: IMFASFStreamSelector::GetBandwidthStepCount
author: windows-sdk-content
description: Retrieves the number of bandwidth steps that exist for the content. This method is used for multiple bit rate (MBR) content.
old-location: mf\imfasfstreamselector_getbandwidthstepcount.htm
old-project: medfound
ms.assetid: 6b7105c1-7395-462f-ad52-daf621258714
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 6b7105c1-7395-462f-ad52-daf621258714, GetBandwidthStepCount, GetBandwidthStepCount method [Media Foundation], GetBandwidthStepCount method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetBandwidthStepCount method, IMFASFStreamSelector.GetBandwidthStepCount, IMFASFStreamSelector::GetBandwidthStepCount, mf.imfasfstreamselector_getbandwidthstepcount, wmcontainer/IMFASFStreamSelector::GetBandwidthStepCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFStreamSelector.GetBandwidthStepCount
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFStreamSelector::GetBandwidthStepCount


## -description



Retrieves the number of bandwidth steps that exist for the content. This method is used for multiple bit rate (MBR) content.




## -parameters




### -param pcStepCount [out]

Receives the number of bandwidth steps.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Bandwidth steps are bandwidth levels used for multiple bit rate (MBR) content. If you stream MBR content, you can choose the bandwidth step that matches the network conditions to avoid interruptions during playback.




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>



<a href="https://msdn.microsoft.com/82d9b642-48e3-4ef5-b0e1-b72f1dd39b2c">IMFASFStreamSelector::GetBandwidthStep</a>
 

 

