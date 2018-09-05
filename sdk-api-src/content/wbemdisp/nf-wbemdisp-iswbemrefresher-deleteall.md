---
UID: NF:wbemdisp.ISWbemRefresher.DeleteAll
title: ISWbemRefresher::DeleteAll
author: windows-sdk-content
description: The SWbemRefresher.DeleteAll method removes all the items from the collection in the SWbemRefresher object.SWbemRefresher object.
old-location: wmi\swbemrefresher_deleteall.htm
old-project: WmiSdk
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: DeleteAll, DeleteAll method [Windows Management Instrumentation], DeleteAll method [Windows Management Instrumentation],ISWbemRefresher interface, DeleteAll method [Windows Management Instrumentation],SWbemRefresher object, ISWbemRefresher interface [Windows Management Instrumentation],DeleteAll method, ISWbemRefresher.DeleteAll, ISWbemRefresher::DeleteAll, SWbemRefresher object [Windows Management Instrumentation],DeleteAll method, SWbemRefresher.DeleteAll, _hmm_swbemrefresher.deleteall, wmi.swbemrefresher_deleteall
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
 - SWbemRefresher.DeleteAll
 - ISWbemRefresher.DeleteAll
 - ISWbemRefresher.DeleteAll
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefresher::DeleteAll


## -description



The <b>SWbemRefresher.DeleteAll</b> method removes all the items from the collection in the 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object.



For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters






## -returns



This method does not return a value.




## -remarks



The corresponding 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> for each removed item has its 
<a href="https://msdn.microsoft.com/238722e0-63e6-4907-993e-67693746d487">Refresher</a> property set to <b>NULL</b>, which indicates that it no longer has a parent refresher.




## -see-also




<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a>
 

 

