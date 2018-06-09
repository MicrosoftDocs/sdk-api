---
UID: NF:wbemdisp.ISWbemRefreshableItem.Remove
title: ISWbemRefreshableItem::Remove
author: windows-sdk-content
description: The SWbemRefreshableItem.Remove method removes the SWbemRefreshableItem object from the parent SWbemRefresher object.SWbemRefreshableItem object from the parent SWbemRefresher object.
old-location: wmi\swbemrefreshableitem_remove.htm
old-project: WmiSdk
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemRefreshableItem interface [Windows Management Instrumentation],Remove method, ISWbemRefreshableItem.Remove, ISWbemRefreshableItem::Remove, Remove, Remove method [Windows Management Instrumentation], Remove method [Windows Management Instrumentation],ISWbemRefreshableItem interface, Remove method [Windows Management Instrumentation],SWbemRefreshableItem object, SWbemRefreshableItem object [Windows Management Instrumentation],Remove method, SWbemRefreshableItem.Remove, _hmm_swbemrefreshableitem.remove, wmi.swbemrefreshableitem_remove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemRefreshableItem.Remove
 - ISWbemRefreshableItem.Remove
 - ISWbemRefreshableItem.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefreshableItem::Remove


## -description



The <b>SWbemRefreshableItem.Remove</b> method removes the 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> object from the parent <a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object.



For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags






#### - lFlags [in, optional]

This parameter must be set to 0 (zero).


## -returns



This method does not return a value.




## -remarks



<b>Error Codes</b>—If the refresher has no item with the specified index, <b>wbemErrNotFound</b> is generated.




## -see-also




<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a>



<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a>
 

 

