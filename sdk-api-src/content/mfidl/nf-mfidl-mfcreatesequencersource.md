---
UID: NF:mfidl.MFCreateSequencerSource
title: MFCreateSequencerSource function
author: windows-sdk-content
description: Creates the sequencer source.
old-location: mf\mfcreatesequencersource.htm
tech.root: medfound
ms.assetid: e4640731-f262-4ceb-8d17-908c2c6b192e
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: MFCreateSequencerSource, MFCreateSequencerSource function [Media Foundation], e4640731-f262-4ceb-8d17-908c2c6b192e, mf.mfcreatesequencersource, mfidl/MFCreateSequencerSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateSequencerSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateSequencerSource function


## -description



Creates the sequencer source.




## -parameters




### -param pReserved

Reserved. Must be <b>NULL</b>.


### -param ppSequencerSource

Receives a pointer to the <a href="https://msdn.microsoft.com/ba5e8e7b-5b0e-4807-a459-75bd5727d1e2">IMFSequencerSource</a> interface of the sequencer source. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>
 

 

