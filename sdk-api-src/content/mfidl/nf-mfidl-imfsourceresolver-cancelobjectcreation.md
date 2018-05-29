---
UID: NF:mfidl.IMFSourceResolver.CancelObjectCreation
title: IMFSourceResolver::CancelObjectCreation
author: windows-sdk-content
description: Cancels an asynchronous request to create an object.
old-location: mf\imfsourceresolver_cancelobjectcreation.htm
old-project: medfound
ms.assetid: 6a30ac92-a281-4293-8975-987fa25a5318
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 6a30ac92-a281-4293-8975-987fa25a5318, CancelObjectCreation, CancelObjectCreation method [Media Foundation], CancelObjectCreation method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],CancelObjectCreation method, IMFSourceResolver.CancelObjectCreation, IMFSourceResolver::CancelObjectCreation, mf.imfsourceresolver_cancelobjectcreation, mfidl/IMFSourceResolver::CancelObjectCreation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSourceResolver.CancelObjectCreation
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSourceResolver::CancelObjectCreation


## -description



          Cancels an asynchronous request to create an object.
        


## -parameters




### -param pIUnknownCancelCookie






#### - ppIUnknownCancelCookie [in]


            Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppIUnknownCancelCookie</i> parameter of the <a href="https://msdn.microsoft.com/6e218b93-4855-40dd-96cc-c4ee02792c14">IMFSourceResolver::BeginCreateObjectFromByteStream</a> or <a href="https://msdn.microsoft.com/bc97c1fb-d23a-4887-b6ac-0751c254a405">IMFSourceResolver::BeginCreateObjectFromURL</a> method.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        You can use this method to cancel a previous call to <a href="https://msdn.microsoft.com/6e218b93-4855-40dd-96cc-c4ee02792c14">BeginCreateObjectFromByteStream</a> or <a href="https://msdn.microsoft.com/bc97c1fb-d23a-4887-b6ac-0751c254a405">BeginCreateObjectFromURL</a>. Because these methods are asynchronous, however, they might be completed before the operation can be canceled. Therefore, your callback might still be invoked after you call this method.
      

<div class="alert"><b>Note</b>  This method cannot be called remotely.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a>



<a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>
 

 

