---
UID: NF:mergemod.IMsmConfigureModule.ProvideTextData
title: IMsmConfigureModule::ProvideTextData
author: windows-sdk-content
description: The ProvideTextData method retrieves text data from the client tool. For more information, see the ProvideTextData method of the ConfigureModule object.
old-location: setup\imsmconfiguremodule_providetextdata.htm
tech.root: msi
ms.assetid: 81803b47-e1b1-45b7-b59d-aac555b189f7
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMsmConfigureModule interface,ProvideTextData method, IMsmConfigureModule.ProvideTextData, IMsmConfigureModule::ProvideTextData, ProvideTextData, ProvideTextData method, ProvideTextData method,IMsmConfigureModule interface, _msi_providetextdata_function, mergemod/IMsmConfigureModule::ProvideTextData, setup.imsmconfiguremodule_providetextdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmConfigureModule.ProvideTextData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmConfigureModule::ProvideTextData


## -description


The 
<b>ProvideTextData</b> method retrieves text data from the 
client tool. For more information, see the <a href="https://msdn.microsoft.com/286b0b58-1b6a-4d41-89e1-eb9c23bdd788">ProvideTextData</a> method of the 
<a href="https://msdn.microsoft.com/f6240837-7685-4bfe-8a2f-b4428014702a">ConfigureModule</a> object.


## -parameters




### -param Name [in]

If the tool does not provide any configuration data for this value, the function should return S_FALSE. In this case, Mergemod.dll ignores the value of the <i>ConfigData</i> argument and uses the Default value from the ModuleConfiguration table.


### -param ConfigData [out]

The tool should return S_OK and provide the appropriate customization text in <i>ConfigData</i>. The client tool is responsible for allocating the data, but Mergemod.dll is responsible for releasing the memory. This argument must be a <b>BSTR</b> object. <b>LPCWSTR</b> is not accepted.


## -returns



Any return code other than S_OK or S_FALSE causes an error to be logged (if a log is open) and results in the merge failing.




## -remarks



The client may be called no more than once for each record in the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>. Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value. If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

