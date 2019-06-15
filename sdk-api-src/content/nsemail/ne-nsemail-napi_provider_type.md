---
UID: NE:nsemail.napi_provider_type_tag
title: NAPI_PROVIDER_TYPE (nsemail.h)
author: windows-sdk-content
description: Specifies the type of hosting expected for a namespace provider.
old-location: winsock\napi_provider_type.htm
tech.root: WinSock
ms.assetid: 0d845cc5-a84a-43fe-b9e7-d1a9153bae73
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NAPI_PROVIDER_TYPE, NAPI_PROVIDER_TYPE enumeration [Winsock], ProviderType_Application, ProviderType_Service, nsemail/NAPI_PROVIDER_TYPE, nsemail/ProviderType_Application, nsemail/ProviderType_Service, winsock.napi_provider_type
ms.topic: enum
f1_keywords: ["nsemail/NAPI_PROVIDER_TYPE"]
req.header: nsemail.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Nsemail.h
api_name:
 - NAPI_PROVIDER_TYPE
product: Windows
targetos: Windows
req.typenames: NAPI_PROVIDER_TYPE
req.redist: 
ms.custom: 19H1
---

# NAPI_PROVIDER_TYPE enumeration


## -description


The <b>NAPI_PROVIDER_TYPE</b> enumeration specifies the type of hosting expected for a namespace provider. 


## -enum-fields




### -field ProviderType_Application

The namespace provider is expected to be hosted by an application. There may be multiple namespace providers of type <b>ProviderType_Application</b> running at the same time on a local system. 

There may also be multiple instances of the same namespace provider running at the same time on a local system as long as the following conditions are met. Only one instance of the same namespace provider application can be running in a single user session at the same time on the local system. The Windows Sockets infrastructure will select the particular target instance of  a namespace provider based on the identity of the client and the user session where it is running. Clients running as user <b>MyUser</b> in a user session will only be able to contact an instance of the same namespace provider running as <b>MyUser</b> in the same session.


### -field ProviderType_Service

The namespace provider is expected to be hosted by a service. This hosting model is not currently supported.


## -remarks



This enumeration is supported on Windows Vistaand later.

On  Windows Vista and Windows Server 2008, the <b>NAPI_PROVIDER_TYPE</b> enumeration applies only to NS_EMAIL namespace providers. Windows Vista and Windows Server 2008 currently support only namespace providers of type <b>ProviderType_Application</b> providers. On  Windows Vista and Windows Server 2008, this value should always be set to <b>ProviderType_Application</b>.

The <b>NAPI_PROVIDER_TYPE</b> enumeration is used by the <a href="https://docs.microsoft.com/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob_tag">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure to specify the provide type of  an NS_EMAIL namespace provider. Examples of a NS_EMAIL namespace provider of type <b>ProviderType_Application</b> would be instant messaging or email clients. An example of a NS_EMAIL namespace provider of type <b>ProviderType_Service</b> would be the Peer Name Resolution Protocol (PNRP) namespace provider. 

The <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a> functions are used to install a namespace provider for the NS_EMAIL namespace using a <a href="https://docs.microsoft.com/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob_tag">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure. 

The <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a> functions are used to enumerate namespace providers for the NS_EMAIL namespace and retrieve the <a href="https://docs.microsoft.com/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob_tag">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure for  a provider.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob_tag">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a>
 

 

