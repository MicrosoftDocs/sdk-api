---
UID: NN:shobjidl_core.IDataObjectProvider
title: IDataObjectProvider (shobjidl_core.h)
author: windows-sdk-content
description: Provides methods that enable you to set or retrieve a DataPackage object's IDataObject interface, which the DataPackage uses to support interoperability. The DataPackage object is used by an app to provide data to another app.
old-location: shell\IDataObjectProvider.htm
tech.root: shell
ms.assetid: 57A5003A-11DF-42c2-9C00-7DE35898B64D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDataObjectProvider, IDataObjectProvider interface [Windows Shell], IDataObjectProvider interface [Windows Shell],described, shell.IDataObjectProvider, shobjidl_core/IDataObjectProvider
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDataObjectProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataObjectProvider interface


## -description


Provides methods that enable you to set or retrieve a <a href="http://go.microsoft.com/fwlink/p/?linkid=267543">DataPackage</a> object's <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject interface</a>, which the DataPackage uses to support interoperability. The DataPackage object is used by an app to provide data to another app.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataObjectProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDataObjectProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDataObjectProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F3678B2-4B18-4344-ADEE-F0D0A6CE635E">GetDataObject</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> representation of the current <a href="http://go.microsoft.com/fwlink/p/?linkid=267543">DataPackage</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4A7787E5-8C16-4cd2-B46F-67F6F636989B">SetDataObject</a>
</td>
<td align="left" width="63%">
Wraps an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> instance as a Windows Runtime
<a href="http://go.microsoft.com/fwlink/p/?linkid=267543">DataPackage</a>.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Do not implement this interface. An implementation is provided as part of the DataPackage object.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

