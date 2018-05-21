---
UID: NF:ocidl.IAdviseSinkEx.OnViewStatusChange
title: IAdviseSinkEx::OnViewStatusChange
author: windows-driver-content
description: Notifies the sink that a view status of an object has changed.
old-location: com\iadvisesinkex_onviewstatuschange.htm
old-project: com
ms.assetid: 9d5129aa-341c-4c69-8c0c-b7c3e62a57c1
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAdviseSinkEx interface [COM],OnViewStatusChange method, IAdviseSinkEx.OnViewStatusChange, IAdviseSinkEx::OnViewStatusChange, OnViewStatusChange, OnViewStatusChange method [COM], OnViewStatusChange method [COM],IAdviseSinkEx interface, _ole_iadvisesinkex_onviewstatuschange, com.iadvisesinkex_onviewstatuschange, ocidl/IAdviseSinkEx::OnViewStatusChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IAdviseSinkEx.OnViewStatusChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IAdviseSinkEx::OnViewStatusChange


## -description


Notifies the sink that a view status of an object has changed.


## -parameters




### -param dwViewStatus [in]

The new view status. Possible values are from the <a href="https://msdn.microsoft.com/7b3118af-db29-4eb1-9b1b-38a8ebe42f19">VIEWSTATUS</a> enumeration.


## -returns



This method returns S_OK on success.




## -remarks



It is important that objects call the <a href="https://msdn.microsoft.com/f2cb3a5b-826b-428a-9e92-e5d08880bddc">IAdviseSink:OnViewChange</a> method whenever the object's view changes even when the object is in place active. Containers rely on this notification to keep an object's view up-to-date.




## -see-also




<a href="https://msdn.microsoft.com/f2cb3a5b-826b-428a-9e92-e5d08880bddc">IAdviseSink:OnViewChange</a>



<a href="https://msdn.microsoft.com/d1a52353-dd86-4083-9dbc-3a6f363a1a57">IAdviseSinkEx</a>
 

 

