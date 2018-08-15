---
UID: NF:wbemdisp.ISWbemRefreshableItem.get_IsSet
title: ISWbemRefreshableItem::get_IsSet
author: windows-sdk-content
description: The SWbemRefreshableItem.IsSet property is a Boolean value that indicates whether the SWbemRefreshableItem object represents a single object or an object set.SWbemRefreshableItem object represents a single object or an object set.
old-location: wmi\swbemrefreshableitem_isset.htm
old-project: WmiSdk
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemRefreshableItem interface [Windows Management Instrumentation],IsSet property, ISWbemRefreshableItem.get_IsSet, ISWbemRefreshableItem.put_IsSet, ISWbemRefreshableItem::get_IsSet, IsSet property [Windows Management Instrumentation], IsSet property [Windows Management Instrumentation],ISWbemRefreshableItem interface, IsSet property [Windows Management Instrumentation],SWbemRefreshableItem object, SWbemRefreshableItem object [Windows Management Instrumentation],IsSet property, SWbemRefreshableItem.IsSet, _hmm_swbemrefreshableitem.isset, get_IsSet, wmi.swbemrefreshableitem_isset
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
 - SWbemRefreshableItem.IsSet
 - ISWbemRefreshableItem.IsSet
 - ISWbemRefreshableItem.get_IsSet
 - ISWbemRefreshableItem.put_IsSet
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefreshableItem::get_IsSet


## -description



The <b>SWbemRefreshableItem.IsSet</b> property is a Boolean value that indicates whether the 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> object represents a single object or an object set.



For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -remarks



If <b>SWbemRefreshableItem.IsSet</b> is <b>TRUE</b>, then the item represents an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object and the 
<a href="https://msdn.microsoft.com/91a693c0-cde4-4cf6-b85a-662cfd0333e9">Object</a> property will be <b>NULL</b>. If <b>FALSE</b>, the item represents an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object and the 
<b>Object</b> property is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefreshableItem</a>
 

 

