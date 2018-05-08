---
UID: NF:xamlom.IVisualTreeService.UnadviseVisualTreeChange
title: IVisualTreeService::UnadviseVisualTreeChange
author: windows-driver-content
description: Stops listening for changes to the visual tree.
old-location: xaml_diagnostics\ivisualtreeservice_unadvisevisualtreechange.htm
old-project: xaml_diagnostics
ms.assetid: E77CBED8-F214-48AC-903E-F01B6EECA2ED
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: IVisualTreeService interface,UnadviseVisualTreeChange method, IVisualTreeService.UnadviseVisualTreeChange, IVisualTreeService::UnadviseVisualTreeChange, UnadviseVisualTreeChange, UnadviseVisualTreeChange method, UnadviseVisualTreeChange method,IVisualTreeService interface, xaml_diagnostics.ivisualtreeservice_unadvisevisualtreechange, xamlom/IVisualTreeService::UnadviseVisualTreeChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VisualMutationType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xamlom.h
api_name:
-	IVisualTreeService.UnadviseVisualTreeChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IVisualTreeService::UnadviseVisualTreeChange


## -description


Stops listening for changes to the visual tree.


## -parameters




### -param pCallback






#### - *pCallback [in]

The callback to unregister for mutation events.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



<b>UnadviseVisualTreeChange</b> should be called when the caller no longer wants to listen for
    mutation events.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

