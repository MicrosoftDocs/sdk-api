---
UID: NF:mbnapi.IMbnConnectionProfileEvents.OnProfileUpdate
title: IMbnConnectionProfileEvents::OnProfileUpdate
author: windows-sdk-content
description: A notification method that indicates that profile update operation has completed.
old-location: mbn\imbnconnectionprofileevents_onprofileupdatecomplete.htm
old-project: mbn
ms.assetid: eb113544-0c89-4b38-a2f4-c67c639fe8a3
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnConnectionProfileEvents interface [Microsoft Broadband Networks],OnProfileUpdate method, IMbnConnectionProfileEvents.OnProfileUpdate, IMbnConnectionProfileEvents::OnProfileUpdate, OnProfileUpdate, OnProfileUpdate method [Microsoft Broadband Networks], OnProfileUpdate method [Microsoft Broadband Networks],IMbnConnectionProfileEvents interface, mbn.imbnconnectionprofileevents_onprofileupdatecomplete, mbnapi/IMbnConnectionProfileEvents::OnProfileUpdate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnConnectionProfileEvents.OnProfileUpdate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfileEvents::OnProfileUpdate


## -description


A notification method that indicates that profile update operation has completed.


## -parameters




### -param newProfile [in]

An <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interface that represents the profile that has changed.  


## -returns



This method must return <b>S_OK</b>.




## -remarks



<b>OnProfileUpdate</b> is called to notify a registered application of the completion of an operation initiated by a call to the <a href="https://msdn.microsoft.com/3243ffec-1897-4f26-853d-81a7198a892d">UpdateProfile</a> method of the <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interface, or the <a href="https://msdn.microsoft.com/b9c191cc-aa6f-4548-ad4a-f2b9808c5f23">CreateConnectionProfile</a> of the <a href="https://msdn.microsoft.com/a55e4183-f914-4064-a391-3bd31ca59160">IMbnConnectionProfileManager</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/235fa0ef-4fc2-4a36-8ad7-2dceb597498f">IMbnConnectionProfileEvents</a>
 

 

