---
UID: NF:wcmconfig.ISettingsNamespace.Save
title: ISettingsNamespace::Save (wcmconfig.h)
author: windows-sdk-content
description: Updates the settings namespace to persistent and visible.
old-location: smi\isettingsnamespace_save.htm
tech.root: SMI
ms.assetid: 368c1d0b-c8a2-47af-82f8-bcc1ccf8930b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISettingsNamespace interface [SMI],Save method, ISettingsNamespace.Save, ISettingsNamespace::Save, Save, Save method [SMI], Save method [SMI],ISettingsNamespace interface, smi.isettingsnamespace_save, wcmconfig/ISettingsNamespace::Save
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsNamespace.Save
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsNamespace::Save


## -description


Updates the settings namespace to persistent and visible.


## -parameters




### -param PushSettings [in]

 Not used. A flag that controls whether to transfer settings to the registry or to an initialization file.


### -param Result [out]

 A pointer to an <a href="https://msdn.microsoft.com/0bbfd39a-0292-4d8e-ae31-f45aebd326a7">ISettingsResult</a> object that contains any error that may have occurred while saving the namespace.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -see-also




<a href="https://msdn.microsoft.com/a5d7b9ff-eb6f-40be-b246-17189cad92be">ISettingsNamespace</a>
 

 

