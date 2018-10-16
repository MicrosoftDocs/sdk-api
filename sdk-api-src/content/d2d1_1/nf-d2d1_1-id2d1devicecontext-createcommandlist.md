---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateCommandList
title: ID2D1DeviceContext::CreateCommandList
author: windows-sdk-content
description: Creates a ID2D1CommandList object.
old-location: direct2d\id2d1devicecontext_createcommandlist.htm
tech.root: direct2d
ms.assetid: f34710dc-7845-457f-9b27-51ae937d9f74
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CreateCommandList, CreateCommandList method [Direct2D], CreateCommandList method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateCommandList method, ID2D1DeviceContext.CreateCommandList, ID2D1DeviceContext::CreateCommandList, d2d1_1/ID2D1DeviceContext::CreateCommandList, direct2d.id2d1devicecontext_createcommandlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.CreateCommandList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::CreateCommandList


## -description


Creates a <a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a> object.


## -parameters




### -param commandList [out]

Type: <b><a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a>**</b>

When this method returns, contains the address of a pointer to a command list.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
</table>
 




## -remarks



A <a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a> can store Direct2D commands to be displayed later through <a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">ID2D1DeviceContext::DrawImage</a> or through an image brush.




## -see-also




<a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

