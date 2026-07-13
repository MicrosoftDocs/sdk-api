---
UID: NF:wuapi.IAutomaticUpdatesSettings3.get_NonAdministratorsElevated
title: IAutomaticUpdatesSettings3::get_NonAdministratorsElevated (wuapi.h)
description: Gets and sets a Boolean value that indicates whether non-administrators can perform some update-related actions without administrator approval. (Get)
helpviewer_keywords: ["IAutomaticUpdatesSettings3 interface [Windows Update Agent]","NonAdministratorsElevated property","IAutomaticUpdatesSettings3.NonAdministratorsElevated","IAutomaticUpdatesSettings3.get_NonAdministratorsElevated","IAutomaticUpdatesSettings3::NonAdministratorsElevated","IAutomaticUpdatesSettings3::get_NonAdministratorsElevated","IAutomaticUpdatesSettings3::put_NonAdministratorsElevated","NonAdministratorsElevated property [Windows Update Agent]","NonAdministratorsElevated property [Windows Update Agent]","IAutomaticUpdatesSettings3 interface","get_NonAdministratorsElevated","wua.iautomaticupdatessettings3_nonadministratorselevated","wuapi/IAutomaticUpdatesSettings3::NonAdministratorsElevated","wuapi/IAutomaticUpdatesSettings3::get_NonAdministratorsElevated","wuapi/IAutomaticUpdatesSettings3::put_NonAdministratorsElevated"]
old-location: wua\iautomaticupdatessettings3_nonadministratorselevated.htm
tech.root: wua
ms.assetid: 6294d982-e6ed-472d-b94b-c140b423ea88
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings3 interface [Windows Update Agent],NonAdministratorsElevated property, IAutomaticUpdatesSettings3.NonAdministratorsElevated, IAutomaticUpdatesSettings3.get_NonAdministratorsElevated, IAutomaticUpdatesSettings3::NonAdministratorsElevated, IAutomaticUpdatesSettings3::get_NonAdministratorsElevated, IAutomaticUpdatesSettings3::put_NonAdministratorsElevated, NonAdministratorsElevated property [Windows Update Agent], NonAdministratorsElevated property [Windows Update Agent],IAutomaticUpdatesSettings3 interface, get_NonAdministratorsElevated, wua.iautomaticupdatessettings3_nonadministratorselevated, wuapi/IAutomaticUpdatesSettings3::NonAdministratorsElevated, wuapi/IAutomaticUpdatesSettings3::get_NonAdministratorsElevated, wuapi/IAutomaticUpdatesSettings3::put_NonAdministratorsElevated
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
 - IAutomaticUpdatesSettings3::get_NonAdministratorsElevated
 - wuapi/IAutomaticUpdatesSettings3::get_NonAdministratorsElevated
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
 - IAutomaticUpdatesSettings3.NonAdministratorsElevated
 - IAutomaticUpdatesSettings3.get_NonAdministratorsElevated
 - IAutomaticUpdatesSettings3.put_NonAdministratorsElevated
---

# IAutomaticUpdatesSettings3::get_NonAdministratorsElevated


## -description

<p class="CCE_Message">[<b>Set</b> is no longer supported. Also, starting with 
    Windows 10 calls to <b>Get</b> always return <b>VARIANT_TRUE</b>.]


Gets and sets a Boolean value that indicates whether non-administrators can perform some update-related actions without administrator approval.



This property is read/write.

## -parameters

## -remarks

The NonAdministratorsElevated property controls whether non-administrative users are allowed to perform some additional actions without elevation. It is equivalent to the “Allow all users to install updates on this computer” check box in the Windows Update settings dialog.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings3">IAutomaticUpdatesSettings3</a>
