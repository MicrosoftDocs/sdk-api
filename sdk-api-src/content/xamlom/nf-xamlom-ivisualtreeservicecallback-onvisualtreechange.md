---
UID: NF:xamlom.IVisualTreeServiceCallback.OnVisualTreeChange
title: IVisualTreeServiceCallback::OnVisualTreeChange
author: windows-sdk-content
description: Communicates the state of the visual tree when it changes.
old-location: xaml_diagnostics\ivisualtreeservicecallback_onvisualtreechange.htm
old-project: xaml_diagnostics
ms.assetid: 91D128E7-ECCA-426D-A6D6-773672302C6C
ms.author: windowssdkdev
ms.date: 03/19/2018
ms.keywords: IVisualTreeServiceCallback interface,OnVisualTreeChange method, IVisualTreeServiceCallback.OnVisualTreeChange, IVisualTreeServiceCallback::OnVisualTreeChange, OnVisualTreeChange, OnVisualTreeChange method, OnVisualTreeChange method,IVisualTreeServiceCallback interface, xaml_diagnostics.ivisualtreeservicecallback_onvisualtreechange, xamlom/IVisualTreeServiceCallback::OnVisualTreeChange
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VisualMutationType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xamlom.h
api_name:
-	IVisualTreeServiceCallback.OnVisualTreeChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IVisualTreeServiceCallback::OnVisualTreeChange


## -description


Communicates the state of the visual tree when it changes.


## -parameters




### -param relation [in]

The association of  a parent object with a child object.


### -param element [in]

The XAML element in the visual tree.


### -param mutationType [in]

A value that indicates whether the change was an add or remove.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/85B94DA2-11EF-49ED-8076-DA5AB36EF781">IVisualTreeServiceCallback</a>
 

 

