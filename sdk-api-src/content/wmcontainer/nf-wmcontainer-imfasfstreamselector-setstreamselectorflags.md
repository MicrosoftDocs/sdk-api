---
UID: NF:wmcontainer.IMFASFStreamSelector.SetStreamSelectorFlags
title: IMFASFStreamSelector::SetStreamSelectorFlags
author: windows-driver-content
description: Sets options for the stream selector.
old-location: mf\imfasfstreamselector_setstreamselectorflags.htm
old-project: medfound
ms.assetid: a2a0f318-0de2-49e0-b8f2-847ab1371752
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFASFStreamSelector interface [Media Foundation],SetStreamSelectorFlags method, IMFASFStreamSelector.SetStreamSelectorFlags, IMFASFStreamSelector::SetStreamSelectorFlags, SetStreamSelectorFlags, SetStreamSelectorFlags method [Media Foundation], SetStreamSelectorFlags method [Media Foundation],IMFASFStreamSelector interface, a2a0f318-0de2-49e0-b8f2-847ab1371752, mf.imfasfstreamselector_setstreamselectorflags, wmcontainer/IMFASFStreamSelector::SetStreamSelectorFlags
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
-	IMFASFStreamSelector.SetStreamSelectorFlags
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFStreamSelector::SetStreamSelectorFlags


## -description



Sets options for the stream selector.




## -parameters




### -param dwStreamSelectorFlags [in]

Bitwise <b>OR</b> of zero or more members of the <a href="https://msdn.microsoft.com/2ececb4a-9516-4066-bf01-0924252f93ee">MFASF_STREAMSELECTOR_FLAGS</a> enumeration specifying the options to use.


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
 

 

