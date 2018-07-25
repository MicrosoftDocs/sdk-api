---
UID: NF:mmc.IConsole.QueryResultView
title: IConsole::QueryResultView
author: windows-sdk-content
description: The IConsole2::QueryResultView method queries IConsole2 for the result view object IUnknown interface pointer.
old-location: mmc\iconsole2_queryresultview.htm
old-project: mmc
ms.assetid: 26d4859c-e79f-4c63-92ad-b66de7d0fa13
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: IConsole interface [MMC],QueryResultView method, IConsole.QueryResultView, IConsole2 interface [MMC],QueryResultView method, IConsole2::QueryResultView, IConsole3 interface [MMC],QueryResultView method, IConsole3::QueryResultView, IConsole::QueryResultView, QueryResultView, QueryResultView method [MMC], QueryResultView method [MMC],IConsole interface, QueryResultView method [MMC],IConsole2 interface, QueryResultView method [MMC],IConsole3 interface, _slate_iconsole2_queryresultview, mmc.iconsole2_queryresultview, mmc/IConsole2::QueryResultView, mmc/IConsole3::QueryResultView, mmc/IConsole::QueryResultView
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole2.QueryResultView
 - IConsole.QueryResultView
 - IConsole3.QueryResultView
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsole::QueryResultView


## -description


The <b>IConsole2::QueryResultView</b> method queries 
<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a> for the result view object 
<a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer.


## -parameters




### -param pUnknown [out]

A pointer to the location of the <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer to the result view object.


## -returns



This method can return one of these values.




## -remarks



<b>QueryResultView</b> can be used when the result view is an OLE custom control (OCX) that implements the 
<a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> interface. The user should call 
<b>QueryResultView</b> to get the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer to the OCX. This is necessary because the Node Manager handles the creation of the OCX.




## -see-also




<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>



<a href="https://msdn.microsoft.com/be3d42a4-a18a-40a5-99fc-2cf2a848c564">IConsole3</a>
 

 

