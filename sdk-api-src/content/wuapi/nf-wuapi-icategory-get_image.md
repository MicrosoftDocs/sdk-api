---
UID: NF:wuapi.ICategory.get_Image
title: ICategory::get_Image (wuapi.h)
author: windows-sdk-content
description: Gets an interface that contains information about the image that is associated with the category.
old-location: wua\icategory_image.htm
tech.root: Wua_Sdk
ms.assetid: 41f0dd44-c919-4264-8f35-ea4e48fd5503
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICategory interface [Windows Update Agent],Image property, ICategory.Image, ICategory.get_Image, ICategory::Image, ICategory::get_Image, Image property [Windows Update Agent], Image property [Windows Update Agent],ICategory interface, get_Image, wua.icategory_image, wuapi/ICategory::Image, wuapi/ICategory::get_Image
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
 - ICategory.Image
 - ICategory.get_Image
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICategory::get_Image


## -description


Gets an interface that contains information about the image that is associated with the category.

This property is read-only.


## -parameters


## -remarks



A <a href="https://msdn.microsoft.com/25620fc2-25f2-4626-9e41-b44c305c505c">Categories</a> property exists for the <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface. And, a <a href="https://msdn.microsoft.com/b821d608-61c2-4442-8b7e-18e27006602b">Categories</a> property exists for the <a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a> interface. Therefore, the information that is used by the localized properties of the <a href="https://msdn.microsoft.com/1ae4ab27-97f3-494b-acd2-991dccf56011">ICategory</a> interface depends on the Windows Update Agent (WUA) object that owns the <b>ICategory</b> interface.

 If the <a href="https://msdn.microsoft.com/1ae4ab27-97f3-494b-acd2-991dccf56011">ICategory</a> interface is returned from the <a href="https://msdn.microsoft.com/25620fc2-25f2-4626-9e41-b44c305c505c">Categories</a> property of <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>, the <b>ICategory</b> interface follows the localization rules of the <b>IUpdate</b> interface. In this case, if the <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface  is created by using the <a href="https://msdn.microsoft.com/7e7a4aa9-7952-4080-9ac0-9544f959475f">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the language that is specified by the <a href="https://msdn.microsoft.com/30ee1836-ea70-4dd1-b531-a7ca32ca940d">UserLocale</a> property of the <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a> interface of the session that is used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="https://msdn.microsoft.com/30ee1836-ea70-4dd1-b531-a7ca32ca940d">UserLocale</a> property of the <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a> interface, or if the <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface is not  created by using the <a href="https://msdn.microsoft.com/7e7a4aa9-7952-4080-9ac0-9544f959475f">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that the provider of the  update recommends.

If the <a href="https://msdn.microsoft.com/1ae4ab27-97f3-494b-acd2-991dccf56011">ICategory</a> interface is returned from the <a href="https://msdn.microsoft.com/b821d608-61c2-4442-8b7e-18e27006602b">Categories</a> property of the <a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a> interface, the <b>ICategory</b> interface follows the localization rules of the <b>IUpdateHistoryEntry2</b> interface. The information  that   this property returns is for the default UI language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that the provider of the  update recommends.




## -see-also




<a href="https://msdn.microsoft.com/1ae4ab27-97f3-494b-acd2-991dccf56011">ICategory</a>



<a href="https://msdn.microsoft.com/869c10c3-a4d1-4001-86f1-30ebf2abe96f">IImageInformation</a>
 

 

