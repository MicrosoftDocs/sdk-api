---
UID: NF:strmif.IPinConnection.DynamicQueryAccept
title: IPinConnection::DynamicQueryAccept
author: windows-sdk-content
description: The DynamicQueryAccept method queries whether the pin can accept the specified media type while the graph is running with the current connection to this pin.
old-location: dshow\ipinconnection_dynamicqueryaccept.htm
tech.root: DirectShow
ms.assetid: 86a4f18c-4bd0-45d2-bb5a-b0f41cd0ab43
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DynamicQueryAccept, DynamicQueryAccept method [DirectShow], DynamicQueryAccept method [DirectShow],IPinConnection interface, IPinConnection interface [DirectShow],DynamicQueryAccept method, IPinConnection.DynamicQueryAccept, IPinConnection::DynamicQueryAccept, IPinConnectionDynamicQueryAccept, dshow.ipinconnection_dynamicqueryaccept, strmif/IPinConnection::DynamicQueryAccept
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IPinConnection.DynamicQueryAccept
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IPinConnection.DynamicQueryAccept
: 
---

# IPinConnection::DynamicQueryAccept


## -description



The <code>DynamicQueryAccept</code> method queries whether the pin can accept the specified media type while the graph is running with the current connection to this pin.




## -parameters




### -param pmt [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the media type.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Media type is acceptable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_TYPE_NOT_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
Media type is not acceptable.

</td>
</tr>
</table>
 




## -remarks



If this method succeeds, the pin can accept the media type on the next sample or in a call to <a href="https://msdn.microsoft.com/b2013e95-88bc-4f4a-87af-2b13c120ec46">IPin::ReceiveConnection</a>.

An application or filter can call this method to determine whether the filter graph must be reconfigured. If the pin can accept the specified media type, there is no need to reconfigure the graph.

Although the <a href="https://msdn.microsoft.com/ed11eeef-464b-4a75-958b-2bc6dbc7af04">IPin::QueryAccept</a> method also determines whether a pin can accept a format type, it does not guarantee that the pin can switch to that format while the filter is running. If you need to switch formats while the filter is running, call <code>DynamicQueryAccept</code> instead.




## -see-also




<a href="https://msdn.microsoft.com/ff60de5a-3edc-405d-aa02-8704b96d5e87">Dynamic Format Changes</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0843a01c-6f6a-4765-abca-dd562175fcee">IPinConnection Interface</a>
 

 

