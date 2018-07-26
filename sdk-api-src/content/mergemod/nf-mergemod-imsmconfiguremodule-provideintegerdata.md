---
UID: NF:mergemod.IMsmConfigureModule.ProvideIntegerData
title: IMsmConfigureModule::ProvideIntegerData
author: windows-sdk-content
description: The ProvideIntegerData method of the ConfigureModule object is called by Mergemod.dll to retrieve integer data from the client tool.
old-location: setup\configuremodule_provideintegerdata.htm
old-project: Msi
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ConfigureModule object,ProvideIntegerData method, ConfigureModule.ProvideIntegerData, IMsmConfigureModule.ProvideIntegerData, IMsmConfigureModule::ProvideIntegerData, ProvideIntegerData, ProvideIntegerData method, ProvideIntegerData method,ConfigureModule object, _msi_provideintegerdata_method, setup.configuremodule_provideintegerdata
ms.prod: windows
ms.technology: windows-sdk
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
 - ConfigureModule.ProvideIntegerData
 - IMsmConfigureModule.ProvideIntegerData
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmConfigureModule::ProvideIntegerData


## -description


The 
<b>ProvideIntegerData</b> method of the 
<a href="https://msdn.microsoft.com/f6240837-7685-4bfe-8a2f-b4428014702a">ConfigureModule object</a> is called by Mergemod.dll to retrieve integer data from the client tool.

Mergemod.dll provides the <i>Name</i> from the corresponding entry in the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>.

The tool should return S_OK and provide the appropriate customization integer in <i>ConfigData</i>.

If the tool does not provide any configuration data for this <i>Name</i> value, the function should return S_FALSE. In this case Mergemod.dll ignores the value of the <i>ConfigData</i> argument and uses the Default value from the ModuleConfiguration table.


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
<a href="https://msdn.microsoft.com/2d03ce35-2ded-4f65-a73f-2546d67b0454">ProvideIntegerData function</a>.



