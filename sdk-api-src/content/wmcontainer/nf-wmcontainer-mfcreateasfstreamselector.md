---
UID: NF:wmcontainer.MFCreateASFStreamSelector
title: MFCreateASFStreamSelector function
author: windows-sdk-content
description: Creates the ASF stream selector.
old-location: mf\mfcreateasfstreamselector.htm
tech.root: medfound
ms.assetid: 71b1af5b-f127-463f-9720-72e789bb2cd1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 71b1af5b-f127-463f-9720-72e789bb2cd1, MFCreateASFStreamSelector, MFCreateASFStreamSelector function [Media Foundation], mf.mfcreateasfstreamselector, wmcontainer/MFCreateASFStreamSelector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - MFCreateASFStreamSelector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateASFStreamSelector function


## -description



Creates the ASF stream selector.




## -parameters




### -param pIASFProfile

Pointer to the <a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a> interface.


### -param ppSelector

Receives a pointer to the <a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a> interface. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

