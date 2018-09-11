---
UID: NF:wuapi.IUpdateHistoryEntry2.get_Categories
title: IUpdateHistoryEntry2::get_Categories
author: windows-sdk-content
description: Gets a collection of the update categories to which an update belongs.
old-location: wua\iupdatehistoryentry2_categories.htm
tech.root: wua_sdk
ms.assetid: b821d608-61c2-4442-8b7e-18e27006602b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Categories property [Windows Update Agent], Categories property [Windows Update Agent],IUpdateHistoryEntry2 interface, IUpdateHistoryEntry2 interface [Windows Update Agent],Categories property, IUpdateHistoryEntry2.Categories, IUpdateHistoryEntry2.get_Categories, IUpdateHistoryEntry2::Categories, IUpdateHistoryEntry2::get_Categories, get_Categories, wua.iupdatehistoryentry2_categories, wuapi/IUpdateHistoryEntry2::Categories, wuapi/IUpdateHistoryEntry2::get_Categories
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateHistoryEntry2.Categories
 - IUpdateHistoryEntry2.get_Categories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateHistoryEntry2::get_Categories


## -description


Gets a collection of the update categories to which an update belongs.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a> interface  may require you to update Windows Update Agent (WUA). For more information, see <a href="https://msdn.microsoft.com/829112ab-b240-4cc4-8053-18b484934886">Updating Windows Update Agent</a>.

The information that this property returns is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language that  the provider of the  update recommends.

Because there is a <a href="https://msdn.microsoft.com/25620fc2-25f2-4626-9e41-b44c305c505c">Categories</a> property of the <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface and a <b>Categories</b> property of the <a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a> interface, the information that is used by the localized properties of the <a href="https://msdn.microsoft.com/1ae4ab27-97f3-494b-acd2-991dccf56011">ICategory</a> interface depends on the WUA object that owns the <b>ICategory</b> interface. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdate</b>, it follows the localization rules of <b>IUpdate</b>. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdateHistoryEntry2</b>, it follows the localization rules of <b>IUpdateHistoryEntry2</b>.




## -see-also




<a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a>
 

 

