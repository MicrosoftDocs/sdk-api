---
UID: NS:mi._MI_ProviderFT
title: MI_ProviderFT (mi.h)
author: windows-sdk-content
description: A support structure used in the MI_ClassDecl and MI_Module structures.
old-location: wmi_v2\mi_providerft.htm
tech.root: wmi_v2
ms.assetid: 494eb3cb-6476-4fe3-8da4-dc7112c6f62f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_ProviderFT, MI_ProviderFT structure [Windows Management Infrastructure (MI)], mi/MI_ProviderFT, wmi_v2.mi_providerft
ms.topic: struct
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ProviderFT
product: Windows
targetos: Windows
req.typenames: MI_ProviderFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_ProviderFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/8e2e2838-5d08-4e51-be96-0928042ccb9f">MI_ClassDecl</a> and <a href="https://msdn.microsoft.com/76a034eb-f5e0-4da2-9c9d-99e196c17da5">MI_Module</a> structures.


## -struct-fields




### -field Load

The server invokes this function to initialize the provider, which
 performs initialization activities.


### -field Unload

The server invokes this function to release any resources held by the 
 provider.


### -field GetInstance

The server invokes this function to obtain a single CIM 
 instance from the provider.


### -field EnumerateInstances

The server calls this function to enumerate instances of a CIM class 
 in the target namespace.


### -field CreateInstance

The server calls this function to create a single CIM 
 instance in the target namespace.


### -field ModifyInstance

The server calls this function to modify an existing CIM 
 instance in the target namespace. The instance must already exist.


### -field DeleteInstance

The server calls this function to delete a single CIM 
 instance from the target namespace.


### -field AssociatorInstances

The server calls this function to find all CIM instances
 associated with a particular 'source' CIM instance.


### -field ReferenceInstances

The server calls this function to enumerate association 
 instances that refer to a particular CIM instance.


### -field EnableIndications

The server calls this function to enable indications delivery 
 from the provider.


### -field DisableIndications

The server calls this function to disable indications delivery 
 from the provider.


### -field Subscribe

The server invokes this function to subscribe to indications.


### -field Unsubscribe

The server invokes this function to unsubscribe from indications.


### -field Invoke

The server calls this function to carry out a CIM extrinsic method 
 invocation on behalf of a requestor.


## -see-also




<a href="https://msdn.microsoft.com/91301D6A-9A13-4898-A923-DB02ACEC9F68">MI_ProviderFT_AssociatorInstances</a>



<a href="https://msdn.microsoft.com/A2502252-A519-45C9-8CA3-661A0E36C0F6">MI_ProviderFT_CreateInstance</a>



<a href="https://msdn.microsoft.com/D4F51943-D1B4-42E5-A798-C76D4973EA01">MI_ProviderFT_DeleteInstance</a>



<a href="https://msdn.microsoft.com/AEBD1588-F7CF-44AA-ADEC-BFA9A7690DBB">MI_ProviderFT_DisableIndications</a>



<a href="https://msdn.microsoft.com/009E9BC7-75F3-4FC5-AA93-35704E5A31CD">MI_ProviderFT_EnableIndications</a>



<a href="https://msdn.microsoft.com/5BBACC7B-FB82-4E1B-9FDD-790BD2504708">MI_ProviderFT_EnumerateInstances</a>



<a href="https://msdn.microsoft.com/0BF77CC5-AA21-424E-9A2D-A31C1F48793D">MI_ProviderFT_GetInstance</a>



<a href="https://msdn.microsoft.com/998B048C-D8DC-47F0-A593-DFA82846B647">MI_ProviderFT_Invoke</a>



<a href="https://msdn.microsoft.com/CD0A5D2C-8877-488D-9F9C-658FC3AEF76F">MI_ProviderFT_Load</a>



<a href="https://msdn.microsoft.com/D653E9C1-0DC4-44F7-B5EE-AB0C2DC37701">MI_ProviderFT_ModifyInstance</a>



<a href="https://msdn.microsoft.com/6F054C86-71A1-43EF-AA60-12D0AF353B5F">MI_ProviderFT_ReferenceInstances</a>



<a href="https://msdn.microsoft.com/C23CD295-254D-4239-BD8E-9EC01C52A724">MI_ProviderFT_Subscribe</a>



<a href="https://msdn.microsoft.com/D539EF50-D5A3-433C-BF05-DDD9F0026A18">MI_ProviderFT_Unload</a>



<a href="https://msdn.microsoft.com/F0D265FC-8E4D-4936-9513-07278A6AA8C3">MI_ProviderFT_Unsubscribe</a>
 

 

