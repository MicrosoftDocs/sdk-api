---
UID: NF:wmcontainer.MFCreateASFSplitter
title: MFCreateASFSplitter function
author: windows-sdk-content
description: Creates the ASF Splitter.
old-location: mf\mfcreateasfsplitter.htm
tech.root: medfound
ms.assetid: 05936a66-ed39-4645-adfb-5816b9981771
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 05936a66-ed39-4645-adfb-5816b9981771, MFCreateASFSplitter, MFCreateASFSplitter function [Media Foundation], mf.mfcreateasfsplitter, wmcontainer/MFCreateASFSplitter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFCreateASFSplitter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateASFSplitter function


## -description



Creates the <a href="https://msdn.microsoft.com/383b1cc6-4a77-4e0e-a766-6213c64b025c">ASF Splitter</a>.




## -parameters




### -param ppISplitter

Receives a pointer to the <a href="https://msdn.microsoft.com/75d8b2a3-7c50-4dd5-8927-b11eb9f12602">IMFASFSplitter</a> interface. The caller must release the interface.


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
 

 

