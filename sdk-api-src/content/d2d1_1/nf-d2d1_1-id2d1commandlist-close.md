---
UID: NF:d2d1_1.ID2D1CommandList.Close
title: ID2D1CommandList::Close
author: windows-sdk-content
description: Instructs the command list to stop accepting commands so that you can use it as an input to an effect or in a call to ID2D1DeviceContext::DrawImage.
old-location: direct2d\id2d1commandlist_close.htm
tech.root: direct2d
ms.assetid: 161A8E33-25C7-4007-8397-D86EBA777D4D
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: Close, Close method [Direct2D], Close method [Direct2D],ID2D1CommandList interface, ID2D1CommandList interface [Direct2D],Close method, ID2D1CommandList.Close, ID2D1CommandList::Close, d2d1_1/ID2D1CommandList::Close, direct2d.id2d1commandlist_close
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
 - ID2D1CommandList.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandList::Close


## -description


Instructs the command list to stop accepting commands so that you can use it as an input to an effect or in a call to <a href="https://msdn.microsoft.com/1235dd6d-8495-4a92-96b7-4d741d9e296f">ID2D1DeviceContext::DrawImage</a>.  You should call the method after it has been attached to an <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>  and written to but before the command list is used.


## -parameters






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
<td>D2DERR_WRONG_STATE </td>
<td>Close has already been called on the command list.</td>
</tr>
</table>
 


<div class="alert"><b>Note</b>  If the device context associated with the command list has an error, the command list returns the same error.</div>
<div> </div>





## -remarks



This method returns D2DERR_WRONG_STATE if it has already been called on the command list. If an error occurred on the device context during population, the method returns that error. Otherwise, the method returns S_OK. 

If the <b>Close</b> method returns an error, any future use of the command list results in the same error.




## -see-also




<a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a>
 

 

