---
UID: NF:strmif.IGraphBuilder.Connect
title: IGraphBuilder::Connect
author: windows-sdk-content
description: The Connect method connects the two pins, using intermediates if necessary.
old-location: dshow\igraphbuilder_connect.htm
old-project: DirectShow
ms.assetid: 8ddcbb73-8220-4d70-9ab3-58d99fa8a958
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: Connect, Connect method [DirectShow], Connect method [DirectShow],IGraphBuilder interface, IGraphBuilder interface [DirectShow],Connect method, IGraphBuilder.Connect, IGraphBuilder::Connect, IGraphBuilderConnect, dshow.igraphbuilder_connect, strmif/IGraphBuilder::Connect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IGraphBuilder.Connect
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphBuilder::Connect


## -description



The <code>Connect</code> method connects the two pins, using intermediates if necessary.




## -parameters




### -param ppinOut [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface on the output pin.


### -param ppinIn [in]

Pointer to the <b>IPin</b> interface on the input pin.


## -returns



Returns an <b>HRESULT</b>. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_PARTIAL_RENDER</b></dt>
</dl>
</td>
<td width="60%">
Partial success; some of the streams from this pin use an unsupported format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Operation aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CANNOT_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
No combination of intermediate filters could be found to make the connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
At least one of the filters is not in the filter graph.

</td>
</tr>
</table>
 




## -remarks



This method connects two pins directly or indirectly, adding intermediate filters if necessary. The method starts by attempting a direct connection. If that fails, it tries to use any filters that are already in the filter graph and have unconnected input pins. (It enumerates these in an arbitrary order.) If that fails, it searches for filters in the registry, and tries them in order of merit. For more information, see <a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>.

During the connection process, the Filter Graph Manager ignores pins on intermediate filters if the pin name begins with a tilde (~). For more information, see <a href="https://msdn.microsoft.com/67a837f3-8b81-4651-a0fa-fed7b61e71c2">PIN_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder Interface</a>
 

 

