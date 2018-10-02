---
UID: NF:mmc.IConsole.QueryResultView
title: IConsole::QueryResultView
author: windows-sdk-content
description: Queries IConsole for the result view object IUnknown interface pointer.
old-location: mmc\iconsole_queryresultview.htm
tech.root: MMC
ms.assetid: A13410D1-38F3-489A-8AAC-BD2909341ACB
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IConsole interface [MMC],QueryResultView method, IConsole.QueryResultView, IConsole::QueryResultView, QueryResultView, QueryResultView method [MMC], QueryResultView method [MMC],IConsole interface, mmc.iconsole_queryresultview, mmc/IConsole::QueryResultView
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole.QueryResultView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsole::QueryResultView


## -description


Queries 
<a href="https://msdn.microsoft.com/edd98f5e-e251-40ff-8136-02bf1b9ea670">IConsole</a> for the result view object 
<a href="_com_iunknown">IUnknown</a> interface pointer.


## -parameters




### -param pUnknown [out]

A pointer to the location of the <a href="_com_iunknown">IUnknown</a> interface pointer to the result view object.


## -returns



This method can return one of these values.




## -remarks



<b>QueryResultView</b> can be used when the result view is an OLE custom control (OCX) that implements the 
<a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> interface. The user should call 
<b>QueryResultView</b> to get the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer to the OCX. This is necessary because the Node Manager handles the creation of the OCX.




## -see-also




<a href="https://msdn.microsoft.com/edd98f5e-e251-40ff-8136-02bf1b9ea670">IConsole</a>
 

 

