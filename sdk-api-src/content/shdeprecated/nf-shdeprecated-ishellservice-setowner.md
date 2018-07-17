---
UID: NF:shdeprecated.IShellService.SetOwner
title: IShellService::SetOwner
author: windows-sdk-content
description: Deprecated. Declares an owner reference to the service object.
old-location: shell\IShellService_SetOwner.htm
old-project: shell
ms.assetid: ef3865b2-b651-4072-86f2-2996fce061a4
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IShellService interface [Windows Shell],SetOwner method, IShellService.SetOwner, IShellService::SetOwner, SetOwner, SetOwner method [Windows Shell], SetOwner method [Windows Shell],IShellService interface, shdeprecated/IShellService::SetOwner, shell.IShellService_SetOwner, zone_IShellService_SetOwner
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IShellService.SetOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IShellService::SetOwner


## -description


Deprecated. Declares an owner reference to the service object.


## -parameters




### -param punkOwner

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>


          The address of an interface pointer to the owner object. If <b>NULL</b>, the object should call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> to release the existing reference.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The client calls <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> for <a href="https://msdn.microsoft.com/0b845907-a879-4f87-a6f5-8cc86dfe03ff">IShellService</a>, then calls <b>SetOwner(this)</b> to declare ownership. When the client is dismissed, typically when the window is closed, it calls <b>SetOwner(NULL)</b> to instruct the service object to release the reference to the owner object.
      



