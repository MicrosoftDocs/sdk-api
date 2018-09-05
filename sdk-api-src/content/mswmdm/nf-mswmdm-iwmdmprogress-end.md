---
UID: NF:mswmdm.IWMDMProgress.End
title: IWMDMProgress::End
author: windows-sdk-content
description: The End method indicates that an operation is finished.
old-location: wmdm\iwmdmprogress_end.htm
old-project: WMDM
ms.assetid: 0edddd8c-8144-40dc-801c-eb8c899be249
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: End, End method [windows Media Device Manager], End method [windows Media Device Manager],IWMDMProgress interface, IWMDMProgress interface [windows Media Device Manager],End method, IWMDMProgress.End, IWMDMProgress::End, IWMDMProgressEnd, mswmdm/IWMDMProgress::End, wmdm.iwmdmprogress_end
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMProgress.End
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMProgress::End


## -description



The <b>End</b> method indicates that an operation is finished.




## -parameters






## -returns



The return value from the method is ignored by Windows Media Device Manager.




## -remarks



This method is called by various interfaces to indicate that an operation is ending. Windows Media Device Manager ignores any return code returned by the <b>End</b> method because the operation is completed or terminated before this method is called.


#### Examples

The following C++ code is an implementation of the <b>End</b> method

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT End()
{
    // TODO: Display the message: "IWMDMProgress::End called."
    return S_OK; // Unnecessary, since this is ignored.
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress Interface</a>



<a href="https://msdn.microsoft.com/85265eb7-0702-4890-b6cb-b247296fe392">IWMDMProgress2::End2</a>



<a href="https://msdn.microsoft.com/fb09cfa8-1a96-412f-a97a-6cc1638b0c77">IWMDMProgress3::End3</a>
 

 

