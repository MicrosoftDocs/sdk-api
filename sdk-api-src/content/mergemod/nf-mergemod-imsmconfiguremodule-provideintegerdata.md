---
UID: NF:mergemod.IMsmConfigureModule.ProvideIntegerData
title: IMsmConfigureModule::ProvideIntegerData method
author: windows-driver-content
description: The ProvideIntegerData method retrieves integer data from the client tool. For more information, see the ProvideIntegerData method of the ConfigureModule object.
old-location: setup\imsmconfiguremodule_provideintegerdata.htm
old-project: Msi
ms.assetid: 2d03ce35-2ded-4f65-a73f-2546d67b0454
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMsmConfigureModule, IMsmConfigureModule interface, ProvideIntegerData method, IMsmConfigureModule::ProvideIntegerData, ProvideIntegerData method, ProvideIntegerData method, IMsmConfigureModule interface, ProvideIntegerData,IMsmConfigureModule.ProvideIntegerData, _msi_provideintegerdata_function, mergemod/IMsmConfigureModule::ProvideIntegerData, setup.imsmconfiguremodule_provideintegerdata
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
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mergemod.dll
api_name:
-	IMsmConfigureModule.ProvideIntegerData
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmConfigureModule::ProvideIntegerData method


## -description


The 
<b>ProvideIntegerData</b> method retrieves integer data from the client tool. For more information, see the 
<a href="https://msdn.microsoft.com/13d48301-bd63-432c-b663-85a840886dda">ProvideIntegerData</a> method of the 
<a href="https://msdn.microsoft.com/f6240837-7685-4bfe-8a2f-b4428014702a">ConfigureModule</a> object.


## -parameters




### -param Name [in]

If the tool does not need to provide any configuration data for this Name value, the function should return S_FALSE. In this case Mergemod.dll ignores the value of the <i>ConfigData</i> argument and will use the Default value from the ModuleConfiguration table.


### -param ConfigData [out]

The tool should return S_OK and provide the appropriate customization text in <i>ConfigData</i>. The client tool is responsible for allocating the data, but Mergemod.dll is responsible for releasing the memory.


## -returns



Any return code other than S_OK or S_FALSE causes an error to be logged (if a log is open) and results in the merge failing.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The tool does not need to provide configuration data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Function succeeded.

</td>
</tr>
</table>
 




## -remarks



The client may be called no more than once for each record in the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>. Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value. If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

