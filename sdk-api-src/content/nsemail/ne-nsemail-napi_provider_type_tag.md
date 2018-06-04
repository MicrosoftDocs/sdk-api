---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# napi_provider_type_tag enumeration


## -description


The <b>NAPI_PROVIDER_TYPE</b> enumeration specifies the type of hosting expected for a namespace provider. 


## -enum-fields




### -field ProviderType_Application

The namespace provider is expected to be hosted by an application. There may be multiple namespace providers of type <b>ProviderType_Application</b> running at the same time on a local system. 

There may also be multiple instances of the same namespace provider running at the same time on a local system as long as the following conditions are met. Only one instance of the same namespace provider application can be running in a single user session at the same time on the local system. The Windows Sockets infrastructure will select the particular target instance of  a namespace provider based on the identity of the client and the user session where it is running. Clients running as user <b>MyUser</b> in a user session will only be able to contact an instance of the same namespace provider running as <b>MyUser</b> in the same session.


### -field ProviderType_Service

The namespace provider is expected to be hosted by a service. This hosting model is not currently supported.


## -remarks



This enumeration is supported on Windows Vista
  and later.

On  Windows Vista and Windows Server 2008, the <b>NAPI_PROVIDER_TYPE</b> enumeration applies only to NS_EMAIL namespace providers. Windows Vista and Windows Server 2008 currently support only namespace providers of type <b>ProviderType_Application</b> providers. On  Windows Vista and Windows Server 2008, this value should always be set to <b>ProviderType_Application</b>.

The <b>NAPI_PROVIDER_TYPE</b> enumeration is used by the <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure to specify the provide type of  an NS_EMAIL namespace provider. Examples of a NS_EMAIL namespace provider of type <b>ProviderType_Application</b> would be instant messaging or email clients. An example of a NS_EMAIL namespace provider of type <b>ProviderType_Service</b> would be the Peer Name Resolution Protocol (PNRP) namespace provider. 

The <a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx</a> and <a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a> functions are used to install a namespace provider for the NS_EMAIL namespace using a <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure. 

The <a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a> and <a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a> functions are used to enumerate namespace providers for the NS_EMAIL namespace and retrieve the <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure for  a provider.




## -see-also




<a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a>



<a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx</a>



<a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a>
 

 

