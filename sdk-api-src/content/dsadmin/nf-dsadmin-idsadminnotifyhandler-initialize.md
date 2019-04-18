---
UID: NF:dsadmin.IDsAdminNotifyHandler.Initialize
title: IDsAdminNotifyHandler::Initialize (dsadmin.h)
author: windows-sdk-content
description: Called to initialize the notification handler.
old-location: ad\idsadminnotifyhandler_initialize.htm
tech.root: ad
ms.assetid: 7fcd49d3-ccdb-4d55-96ea-cc925a36c366
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DSA_NOTIFY_ALL, DSA_NOTIFY_DEL, DSA_NOTIFY_MOV, DSA_NOTIFY_PROP, DSA_NOTIFY_REN, IDsAdminNotifyHandler interface [Active Directory],Initialize method, IDsAdminNotifyHandler.Initialize, IDsAdminNotifyHandler::Initialize, Initialize, Initialize method [Active Directory], Initialize method [Active Directory],IDsAdminNotifyHandler interface, ad.idsadminnotifyhandler_initialize, dsadmin/IDsAdminNotifyHandler::Initialize
ms.topic: method
req.header: dsadmin.h
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
req.type-library: 
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNotifyHandler.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsAdminNotifyHandler::Initialize


## -description


The <b>IDsAdminNotifyHandler::Initialize</b> method is called to initialize the  notification  handler.


## -parameters




### -param pExtraInfo [in]

Reserved. This parameter will be <b>NULL</b>.


### -param puEventFlags [out]

Pointer to a <b>ULONG</b> value that receives a set of flags that indicate which events the notification handler should receive. This can be a combination of one or more of the following values. If this parameter receives zero, the notification handler will not receive any events.



#### DSA_NOTIFY_DEL

Notify the handler when an object is deleted.



#### DSA_NOTIFY_REN

Notify the handler when an object is  renamed.



#### DSA_NOTIFY_MOV

Notify the handler when an object is moved.



#### DSA_NOTIFY_PROP

Notify the handler when a property is changed.



#### DSA_NOTIFY_ALL

Notify the handler in response to all events.


## -returns



If the method succeeds, <b>S_OK</b> is returned. If the method fails,  a standard <b>HRESULT</b> value is returned.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a>



<a href="https://msdn.microsoft.com/d55e1473-8e51-441e-bd22-63208b294e14">IDsAdminNotifyHandler</a>
 

 

