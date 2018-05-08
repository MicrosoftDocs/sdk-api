---
UID: NF:mswmdm.IWMDMProgress2.End2
title: IWMDMProgress2::End2
author: windows-driver-content
description: The End2 method extends IWMDMProgress::End by providing a completion status indicator.
old-location: wmdm\iwmdmprogress2_end2.htm
old-project: WMDM
ms.assetid: 85265eb7-0702-4890-b6cb-b247296fe392
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: End2, End2 method [windows Media Device Manager], End2 method [windows Media Device Manager],IWMDMProgress2 interface, IWMDMProgress2 interface [windows Media Device Manager],End2 method, IWMDMProgress2.End2, IWMDMProgress2::End2, IWMDMProgress2End2, mswmdm/IWMDMProgress2::End2, wmdm.iwmdmprogress2_end2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMProgress2.End2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMProgress2::End2


## -description



The <b>End2</b> method extends <a href="https://msdn.microsoft.com/0edddd8c-8144-40dc-801c-eb8c899be249">IWMDMProgress::End</a> by providing a completion status indicator.




## -parameters




### -param hrCompletionCode [in]

The return value of the operation that ended.


## -returns



The return value from the method is ignored by Windows Media Device Manager.




## -remarks



<b>IWMDMProgress2</b> is a callback interface provided by the application to Windows Media Device Manager for a particular operation. <b>End2</b> is called when that operation is completed. The <i>hrCompletionCode</i> parameter is the completion status of the operation that was in progress. For example, an application can provide an <b>IWMDMProgress2</b> interface pointer to the <b>Insert2</b> method. When the file transfer done by <b>Insert2</b> is completed, <b>End2</b> is called on the <b>IWMDMProgress2</b> interface pointer with the completion status of the file transfer as the <i>hrCompletion</i> parameter.


<a href="https://msdn.microsoft.com/fb09cfa8-1a96-412f-a97a-6cc1638b0c77">IWMDMProgress3::End3</a> provides more information, and should be implemented instead of this method.


#### Examples

The following C++ code is a simple implementation of the <b>Progress2</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Progress(DWORD  dwTranspiredTicks)
{
    // TODO: Display the message: "IWMDMProgress::Progress called." 
    // followed by the dwTranspiredTicks value.
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/59619571-0ab7-42a4-ad25-c420ec9667a3">IWMDMProgress2 Interface</a>



<a href="https://msdn.microsoft.com/fb09cfa8-1a96-412f-a97a-6cc1638b0c77">IWMDMProgress3::End3</a>
 

 

