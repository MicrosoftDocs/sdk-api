---
UID: NS:winsvc._SERVICE_DESCRIPTIONA
title: "_SERVICE_DESCRIPTIONA"
author: windows-sdk-content
description: Contains a service description.
old-location: base\service_description_str.htm
old-project: Services
ms.assetid: 1b4e18d5-6086-4d1b-b39c-1d919bfdc0b9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSERVICE_DESCRIPTIONA, LPSERVICE_DESCRIPTION, LPSERVICE_DESCRIPTION structure pointer, SERVICE_DESCRIPTION, SERVICE_DESCRIPTION structure, SERVICE_DESCRIPTIONA, SERVICE_DESCRIPTIONW, _SERVICE_DESCRIPTIONA, _win32_service_description_str, base.service_description_str, winsvc/LPSERVICE_DESCRIPTION, winsvc/SERVICE_DESCRIPTION, winsvc/SERVICE_DESCRIPTIONA, winsvc/SERVICE_DESCRIPTIONW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsvc.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SERVICE_DESCRIPTIONW (Unicode) and SERVICE_DESCRIPTIONA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SERVICE_DESCRIPTIONA, *LPSERVICE_DESCRIPTIONA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SERVICE_DESCRIPTION
 - SERVICE_DESCRIPTIONA
 - SERVICE_DESCRIPTIONW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SERVICE_DESCRIPTIONA structure


## -description


Contains a service description.


## -struct-fields




### -field lpDescription

The description of the service. If this member is <b>NULL</b>, the description remains unchanged. If this value is an empty string (""), the current description is deleted. 




The service description must not exceed the size of a registry value of type <b>REG_SZ</b>.

This member can specify a localized string using the following format:

@[<i>path</i>\]<i>dllname</i>,-<i>strID</i>

The string with identifier <i>strID</i> is loaded from <i>dllname</i>; the <i>path</i> is optional. For more information, see <a href="https://msdn.microsoft.com/76ffc77f-a1bc-4e01-858f-4a76563a2bbc">RegLoadMUIString</a>.

<b>Windows Server 2003 and Windows XP:  </b>Localized strings are not supported until Windows Vista.


## -remarks



A description of <b>NULL</b> indicates no service description exists. The service description is NULL when the service is created.

The description is simply a comment that explains the purpose of the service. For example, for the DHCP service, you could use the description "Provides internet addresses for computer on your network."

You can set the description using the 
<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a> function. You can retrieve the description using the 
<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a> function. The description is also displayed by the Services snap-in.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/79aa4ad5-87ee-4f5d-9c8e-4e788f4c7182">Changing a Service's Configuration</a> or <a href="https://msdn.microsoft.com/e6633dc9-c9b6-457d-8adc-e751ec9cf71d">Querying a Service's Configuration</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>
 

 

