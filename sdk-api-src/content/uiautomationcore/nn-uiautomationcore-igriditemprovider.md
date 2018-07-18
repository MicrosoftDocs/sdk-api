---
UID: NN:uiautomationcore.IGridItemProvider
title: IGridItemProvider
author: windows-sdk-content
description: Provides access to individual child controls of containers that implement IGridProvider.
old-location: winauto\uiauto_IGridItemProvider.htm
old-project: WinAuto
ms.assetid: 334a10f1-8bfc-4935-9eee-6176a3e8a4f1
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IGridItemProvider, IGridItemProvider interface [Windows Accessibility], IGridItemProvider interface [Windows Accessibility],described, uiauto.uiauto_IGridItemProvider, uiauto_IGridItemProvider, uiautomationcore/IGridItemProvider, winauto.uiauto_IGridItemProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IGridItemProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IGridItemProvider interface


## -description


Provides access 
        to individual child controls of containers that implement <a href="https://msdn.microsoft.com/37e2cc95-d765-4c2c-ae8a-5a072a43ad5a">IGridProvider</a>.


## -remarks




            Implemented on a UI Automation provider that must support the <a href="https://msdn.microsoft.com/ae4b9021-1800-485b-99a2-54ddf9c21f93">GridItem</a> <i>control pattern</i>.
   			


            Controls that implement <b>IGridItemProvider</b> can typically be traversed 
            (that is, a UI Automation client can move to adjacent controls) by using the keyboard.
            




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

