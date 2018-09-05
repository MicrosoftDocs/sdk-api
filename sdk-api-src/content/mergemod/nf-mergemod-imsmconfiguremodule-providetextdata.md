---
UID: NF:mergemod.IMsmConfigureModule.ProvideTextData
title: IMsmConfigureModule::ProvideTextData
author: windows-sdk-content
description: The ProvideTextData method is called by Mergemod.dll to retrieve text data from the client tool. Mergemod.dll provides the Name from the corresponding entry in the ModuleConfiguration table.
old-location: setup\configuremodule_providetextdata.htm
old-project: msi
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ConfigureModule object,ProvideTextData method, ConfigureModule.ProvideTextData, IMsmConfigureModule.ProvideTextData, IMsmConfigureModule::ProvideTextData, ProvideTextData, ProvideTextData method, ProvideTextData method,ConfigureModule object, _msi_providetextdata_method, setup.configuremodule_providetextdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - ConfigureModule.ProvideTextData
 - IMsmConfigureModule.ProvideTextData
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmConfigureModule::ProvideTextData


## -description


The 
<b>ProvideTextData</b> method is called by Mergemod.dll to retrieve text data from the client tool. Mergemod.dll provides the <i>Name</i> from the corresponding entry in the ModuleConfiguration table.

The tool should return S_OK and provide the appropriate customization text in ConfigData. The client tool is responsible for allocating the data, but Mergemod.dllis responsible for releasing the memory. This argument MUST be a <b>BSTR</b> object. <b>LPCWSTR</b> is NOT accepted.

If the tool does not provide any configuration data for this <i>Name</i> value, the function should return S_FALSE. In this case Mergemod.dll ignores the value of the ConfigData argument and uses the Default value from the ModuleConfiguration table.

Any return code other than S_OK or S_FALSE will cause an error to be logged (if a log is open) and will result in the merge failing.

Because this function follows standard <b>BSTR</b> convention, null is equivalent to the empty string.


## -parameters




### -param Name

Name of item for which data is being retrieved.


### -param ConfigData

Pointer to customization text.


## -returns



This method does not return a value.




## -remarks



The client may be called no more than once for each record in the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>. Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value. If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/81803b47-e1b1-45b7-b59d-aac555b189f7">ProvideTextData function</a>.



