---
UID: NF:mmc.IConsole.QueryResultImageList
title: IConsole::QueryResultImageList
author: windows-sdk-content
description: The IConsole2::QueryResultImageList method returns the console-provided result-view image list. This image list should be used only if the snap-in is using the default list view.
old-location: mmc\iconsole2_queryresultimagelist.htm
old-project: mmc
ms.assetid: eaf91ea6-9389-4155-805c-72bbae99ca04
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IConsole interface [MMC],QueryResultImageList method, IConsole.QueryResultImageList, IConsole2 interface [MMC],QueryResultImageList method, IConsole2::QueryResultImageList, IConsole3 interface [MMC],QueryResultImageList method, IConsole3::QueryResultImageList, IConsole::QueryResultImageList, QueryResultImageList, QueryResultImageList method [MMC], QueryResultImageList method [MMC],IConsole interface, QueryResultImageList method [MMC],IConsole2 interface, QueryResultImageList method [MMC],IConsole3 interface, _slate_iconsole2_queryresultimagelist, mmc.iconsole2_queryresultimagelist, mmc/IConsole2::QueryResultImageList, mmc/IConsole3::QueryResultImageList, mmc/IConsole::QueryResultImageList
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
 - IConsole2.QueryResultImageList
 - IConsole.QueryResultImageList
 - IConsole3.QueryResultImageList
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsole::QueryResultImageList


## -description


The <b>IConsole2::QueryResultImageList</b> method returns the console-provided result-view image list. This image list should be used only if the snap-in is using the default list view.


## -parameters




### -param ppImageList [out]

Address of a variable that receives the 
<a href="https://msdn.microsoft.com/a957239b-6cb2-4101-adeb-e9ba4f876af4">IImageList</a> interface pointer.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>



<a href="https://msdn.microsoft.com/be3d42a4-a18a-40a5-99fc-2cf2a848c564">IConsole3</a>



<a href="https://msdn.microsoft.com/a957239b-6cb2-4101-adeb-e9ba4f876af4">IImageList</a>
 

 

