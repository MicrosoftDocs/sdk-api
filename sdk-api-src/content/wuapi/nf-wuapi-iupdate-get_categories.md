---
UID: NF:wuapi.IUpdate.get_Categories
title: IUpdate::get_Categories
author: windows-sdk-content
description: Gets an interface that contains a collection of categories to which the update belongs.
old-location: wua\iupdate_categories.htm
old-project: wua_sdk
ms.assetid: 25620fc2-25f2-4626-9e41-b44c305c505c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Categories property [Windows Update Agent], Categories property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],Categories property, IUpdate.Categories, IUpdate.get_Categories, IUpdate::Categories, IUpdate::get_Categories, get_Categories, wua.iupdate_categories, wuapi/IUpdate::Categories, wuapi/IUpdate::get_Categories
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.Categories
 - IUpdate.get_Categories
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IUpdate::get_Categories


## -description


Gets an interface that contains a  collection of categories to which the update belongs.

This property is read-only.


## -parameters


## -remarks



If the <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface  is  created by using the <a href="https://msdn.microsoft.com/7e7a4aa9-7952-4080-9ac0-9544f959475f">IUpdateSession::CreateUpdateSearcher</a> method, the information  that  this property returns is for the language that is specified by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn923292">UserLocale</a> property of the <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a> interface of the session that was used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn923292">UserLocale</a> property of <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a>, or if the <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface is  not  created by using <a href="https://msdn.microsoft.com/7e7a4aa9-7952-4080-9ac0-9544f959475f">IUpdateSession::CreateUpdateSearcher</a>, the information  that   this property returns is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, Windows Update Agent (WUA) uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that  the provider of the  update recommends.

Because there is a <b>Categories</b> property of <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> and a <a href="https://msdn.microsoft.com/b821d608-61c2-4442-8b7e-18e27006602b">Categories</a> property of <a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a>, the information that is used by the localized properties of the <a href="https://msdn.microsoft.com/1ae4ab27-97f3-494b-acd2-991dccf56011">ICategory</a> interface depend on the WUA object that owns the <b>ICategory</b> interface. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdate</b>, it follows the localization rules of <b>IUpdate</b>. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdateHistoryEntry2</b>, it follows the localization rules of <b>IUpdateHistoryEntry2</b>.




## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

