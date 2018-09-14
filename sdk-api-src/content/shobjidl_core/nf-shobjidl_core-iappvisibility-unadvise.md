---
UID: NF:shobjidl_core.IAppVisibility.Unadvise
title: IAppVisibility::Unadvise
author: windows-sdk-content
description: Cancels a connection that was previously established by using Advise.
old-location: shell\IAppVisibility_Unadvise.htm
tech.root: shell
ms.assetid: D670F1E7-5E0B-498E-8F27-DF2A3A387862
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IAppVisibility interface [Windows Shell],Unadvise method, IAppVisibility.Unadvise, IAppVisibility::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IAppVisibility interface, shell.IAppVisibility_Unadvise, shobjidl_core/IAppVisibility::Unadvise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAppVisibility.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppVisibility::Unadvise


## -description


Cancels a connection that was previously established by using <a href="https://msdn.microsoft.com/602F46EF-014C-4219-9C1F-C1B4371EA456">Advise</a>.


## -parameters




### -param dwCookie [in]

A token that uniquely identifies the connection to cancel, which is provided by a previous call to to the <a href="https://msdn.microsoft.com/602F46EF-014C-4219-9C1F-C1B4371EA456">Advise</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/89E26D36-3536-45F5-9396-83CCFB26890B">IAppVisibility</a>



<a href="https://msdn.microsoft.com/F6BABF7D-FA05-4A68-878F-A27A6990EC3F">IAppVisibilityEvents</a>
 

 

