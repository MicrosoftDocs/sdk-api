---
UID: NF:wuapi.IUpdateSession2.put_UserLocale
title: IUpdateSession2::put_UserLocale (wuapi.h)
author: windows-sdk-content
description: Gets and sets the preferred locale for which update information is retrieved..
old-location: wua\iupdatesession2_userlocale.htm
tech.root: Wua_Sdk
ms.assetid: 30ee1836-ea70-4dd1-b531-a7ca32ca940d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUpdateSession2 interface [Windows Update Agent],UserLocale property, IUpdateSession2.UserLocale, IUpdateSession2.put_UserLocale, IUpdateSession2::UserLocale, IUpdateSession2::get_UserLocale, IUpdateSession2::put_UserLocale, UserLocale property [Windows Update Agent], UserLocale property [Windows Update Agent],IUpdateSession2 interface, put_UserLocale, wua.iupdatesession2_userlocale, wuapi/IUpdateSession2::UserLocale, wuapi/IUpdateSession2::get_UserLocale, wuapi/IUpdateSession2::put_UserLocale
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
 - IUpdateSession2.UserLocale
 - IUpdateSession2.get_UserLocale
 - IUpdateSession2.put_UserLocale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateSession2::put_UserLocale


## -description


Gets and sets the preferred locale for which update information is retrieved.. 

If you do not specify the locale, the default is the user locale that   <a href="https://msdn.microsoft.com/0de3a2d8-e595-4068-805c-b9bcba7ada91">GetUserDefaultUILanguage</a> returns. If the information is not available in a specified locale or in the user locale, Windows Update Agent (WUA) tries to retrieve the information from the default update locale.

This property is read/write.


## -parameters


## -remarks



A search from an <b>UpdateSearch</b> object that was created from the <b>UpdateSession</b> object fails if the following conditions are true:

<ul>
<li>A user or a power user set the <b>UserLocale</b> property for the <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a> interface to a locale.</li>
<li>The locale corresponds to a language that is not installed on the computer.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a>
 

 

