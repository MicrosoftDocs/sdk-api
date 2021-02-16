---
UID: NF:wuapi.IUpdateServiceRegistration.get_IsPendingRegistrationWithAU
title: IUpdateServiceRegistration::get_IsPendingRegistrationWithAU (wuapi.h)
description: Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added.
helpviewer_keywords: ["IUpdateServiceRegistration interface [Windows Update Agent]","IsPendingRegistrationWithAU property","IUpdateServiceRegistration.IsPendingRegistrationWithAU","IUpdateServiceRegistration.get_IsPendingRegistrationWithAU","IUpdateServiceRegistration::IsPendingRegistrationWithAU","IUpdateServiceRegistration::get_IsPendingRegistrationWithAU","IsPendingRegistrationWithAU property [Windows Update Agent]","IsPendingRegistrationWithAU property [Windows Update Agent]","IUpdateServiceRegistration interface","get_IsPendingRegistrationWithAU","wua.iupdateserviceregistration_ispendingregistrationwithau","wuapi/IUpdateServiceRegistration::IsPendingRegistrationWithAU","wuapi/IUpdateServiceRegistration::get_IsPendingRegistrationWithAU"]
old-location: wua\iupdateserviceregistration_ispendingregistrationwithau.htm
tech.root: wua
ms.assetid: abd90925-979a-49ef-b071-ea48b537fee7
ms.date: 12/05/2018
ms.keywords: IUpdateServiceRegistration interface [Windows Update Agent],IsPendingRegistrationWithAU property, IUpdateServiceRegistration.IsPendingRegistrationWithAU, IUpdateServiceRegistration.get_IsPendingRegistrationWithAU, IUpdateServiceRegistration::IsPendingRegistrationWithAU, IUpdateServiceRegistration::get_IsPendingRegistrationWithAU, IsPendingRegistrationWithAU property [Windows Update Agent], IsPendingRegistrationWithAU property [Windows Update Agent],IUpdateServiceRegistration interface, get_IsPendingRegistrationWithAU, wua.iupdateserviceregistration_ispendingregistrationwithau, wuapi/IUpdateServiceRegistration::IsPendingRegistrationWithAU, wuapi/IUpdateServiceRegistration::get_IsPendingRegistrationWithAU
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateServiceRegistration::get_IsPendingRegistrationWithAU
 - wuapi/IUpdateServiceRegistration::get_IsPendingRegistrationWithAU
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateServiceRegistration.IsPendingRegistrationWithAU
 - IUpdateServiceRegistration.get_IsPendingRegistrationWithAU
---

# IUpdateServiceRegistration::get_IsPendingRegistrationWithAU


## -description

Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added. The authorization cabinet file (.cab) of the service determines whether  the service can be added.

This property is read-only.

## -parameters

## -remarks

If the <a href="/windows/desktop/api/wuapi/ne-wuapi-updateserviceregistrationstate">RegistrationState</a> property is <b>usrsRegistrationPending</b>, registration with Automatic Updates is subject to the allowed settings that are specified in the authorization cabinet  file (.cab) for the service.  If the authorization cabinet file does not allow registration with Automatic Updates, the service will  be registered with Windows Update Agent (WUA). However, the service will  not be registered with Automatic Updates.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateserviceregistration">IUpdateServiceRegistration</a>