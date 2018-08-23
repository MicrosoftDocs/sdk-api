---
UID: NF:qnetwork.IAMNetShowExProps.get_SourceProtocol
title: IAMNetShowExProps::get_SourceProtocol
author: windows-sdk-content
description: The get_SourceProtocol method retrieves the source protocol.
old-location: dshow\iamnetshowexprops_get_sourceprotocol.htm
old-project: DirectShow
ms.assetid: 498e81fc-90d3-4a24-b672-c7c62b3bfd39
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMNetShowExProps interface [DirectShow],get_SourceProtocol method, IAMNetShowExProps.get_SourceProtocol, IAMNetShowExProps::get_SourceProtocol, IAMNetShowExPropsget_SourceProtocol, dshow.iamnetshowexprops_get_sourceprotocol, get_SourceProtocol, get_SourceProtocol method [DirectShow], get_SourceProtocol method [DirectShow],IAMNetShowExProps interface, qnetwork/IAMNetShowExProps::get_SourceProtocol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowExProps.get_SourceProtocol
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMNetShowExProps::get_SourceProtocol


## -description



The <code>get_SourceProtocol</code> method retrieves the source protocol.




## -parameters




### -param pSourceProtocol

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Unknown protocol</td>
</tr>
<tr>
<td>1</td>
<td>Multicast</td>
</tr>
<tr>
<td>2</td>
<td>Multisession bridge</td>
</tr>
<tr>
<td>3</td>
<td>UDP</td>
</tr>
<tr>
<td>4</td>
<td>TCP</td>
</tr>
<tr>
<td>5</td>
<td>Media Streaming Broadcast Distribution (MSBD)</td>
</tr>
<tr>
<td>6</td>
<td>HTTP</td>
</tr>
<tr>
<td>7</td>
<td>File</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e68959dc-1a79-4e2c-aeaf-3febcb9c09ce">IAMNetShowExProps Interface</a>
 

 

