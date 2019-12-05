---
UID: NF:mfidl.MFCreateTopology
title: MFCreateTopology function (mfidl.h)
description: Creates a topology object.
old-location: mf\mfcreatetopology.htm
tech.root: medfound
ms.assetid: 9811eca7-e822-4ff7-93e4-2eb6245d4490
ms.date: 12/05/2018
ms.keywords: 9811eca7-e822-4ff7-93e4-2eb6245d4490, MFCreateTopology, MFCreateTopology function [Media Foundation], mf.mfcreatetopology, mfidl/MFCreateTopology
ms.topic: function
f1_keywords:
- mfidl/MFCreateTopology
dev_langs:
- c++
req.header: mfidl.h
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
- MFCreateTopology
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateTopology function


## -description



Creates a topology object.




## -parameters




### -param ppTopo

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the topology object. The caller must release the interface.


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




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topologies">Topologies</a>
 

 

