---
UID: NF:mmc.IConsole.QueryResultImageList
title: IConsole::QueryResultImageList (mmc.h)
description: Retrieves the console-provided result-view image list. This image list should be used only if the snap-in is using the default list view.
old-location: mmc\iconsole_queryresultimagelist.htm
tech.root: mmc
ms.assetid: 86F2A9ED-4023-4425-8C0A-7593660C623C
ms.date: 12/05/2018
ms.keywords: IConsole interface [MMC],QueryResultImageList method, IConsole.QueryResultImageList, IConsole::QueryResultImageList, QueryResultImageList, QueryResultImageList method [MMC], QueryResultImageList method [MMC],IConsole interface, mmc.iconsole_queryresultimagelist, mmc/IConsole::QueryResultImageList
ms.topic: method
f1_keywords:
- mmc/IConsole.QueryResultImageList
dev_langs:
- c++
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
- IConsole.QueryResultImageList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConsole::QueryResultImageList


## -description


Retrieves the console-provided result-view image list. This image list should be used only if the snap-in is using the default list view.


## -parameters




### -param ppImageList [out]

Address of a variable that receives the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iimagelist">IImageList</a> interface pointer.


## -returns



This method can return one of these values.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iimagelist">IImageList</a>
 

 

