---
UID: NF:mfidl.MFCreateTopology
title: MFCreateTopology function
author: windows-sdk-content
description: Creates a topology object.
old-location: mf\mfcreatetopology.htm
tech.root: medfound
ms.assetid: 9811eca7-e822-4ff7-93e4-2eb6245d4490
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 9811eca7-e822-4ff7-93e4-2eb6245d4490, MFCreateTopology, MFCreateTopology function [Media Foundation], mf.mfcreatetopology, mfidl/MFCreateTopology
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateTopology function


## -description



Creates a topology object.




## -parameters




### -param ppTopo

Receives a pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the topology object. The caller must release the interface.


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



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

