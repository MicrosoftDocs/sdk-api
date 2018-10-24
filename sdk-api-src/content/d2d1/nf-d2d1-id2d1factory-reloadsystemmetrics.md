---
UID: NF:d2d1.ID2D1Factory.ReloadSystemMetrics
title: ID2D1Factory::ReloadSystemMetrics
author: windows-sdk-content
description: Forces the factory to refresh any system defaults that it might have changed since factory creation.
old-location: direct2d\ID2D1Factory_ReloadSystemMetrics.htm
tech.root: Direct2D
ms.assetid: 32c831c4-73e1-49f8-8d58-4248ae99fe37
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ID2D1Factory interface [Direct2D],ReloadSystemMetrics method, ID2D1Factory.ReloadSystemMetrics, ID2D1Factory::ReloadSystemMetrics, ReloadSystemMetrics, ReloadSystemMetrics method [Direct2D], ReloadSystemMetrics method [Direct2D],ID2D1Factory interface, d2d1/ID2D1Factory::ReloadSystemMetrics, direct2d.ID2D1Factory_ReloadSystemMetrics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.ReloadSystemMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::ReloadSystemMetrics


## -description


Forces the factory to refresh any system defaults that it might have changed since factory creation.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You should call this method before calling the <a href="https://msdn.microsoft.com/dd46252b-80eb-42c2-a2b4-5c49ef124bd5">GetDesktopDpi</a> method, to ensure that the system DPI is current.




## -see-also




<a href="https://msdn.microsoft.com/dd46252b-80eb-42c2-a2b4-5c49ef124bd5">GetDesktopDpi</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

