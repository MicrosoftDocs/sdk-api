---
UID: NF:wmcontainer.IMFASFStreamSelector.GetOutputOverride
title: IMFASFStreamSelector::GetOutputOverride
author: windows-driver-content
description: Retrieves the manual output override selection that is set for a stream.
old-location: mf\imfasfstreamselector_getoutputoverride.htm
old-project: medfound
ms.assetid: 64413669-bcb9-47fa-9362-b3f6831e55fb
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: 64413669-bcb9-47fa-9362-b3f6831e55fb, GetOutputOverride, GetOutputOverride method [Media Foundation], GetOutputOverride method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetOutputOverride method, IMFASFStreamSelector.GetOutputOverride, IMFASFStreamSelector::GetOutputOverride, mf.imfasfstreamselector_getoutputoverride, wmcontainer/IMFASFStreamSelector::GetOutputOverride
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMFASFStreamSelector.GetOutputOverride
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFStreamSelector::GetOutputOverride


## -description



Retrieves the manual output override selection that is set for a stream.




## -parameters




### -param dwOutputNum [in]

Stream number for which to retrieve the output override selection.


### -param pSelection [out]

Receives the output override selection. The value is a member of the <a href="https://msdn.microsoft.com/1571650b-4d5c-49ae-9e6d-77ef4ae7ae59">ASF_SELECTION_STATUS</a> enumeration.


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
 




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>
 

 

