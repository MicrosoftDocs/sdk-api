---
UID: NF:certadm.IOCSPCAConfigurationCollection.CreateCAConfiguration
title: IOCSPCAConfigurationCollection::CreateCAConfiguration
author: windows-sdk-content
description: Creates a new certification authority (CA) configuration and adds it to the configuration set.
old-location: security\iocspcaconfigurationcollection_createcaconfiguration_method.htm
old-project: seccrypto
ms.assetid: d1c47402-77b1-4c43-8d57-20b9dd2682f7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateCAConfiguration, CreateCAConfiguration method [Security], CreateCAConfiguration method [Security],IOCSPCAConfigurationCollection interface, IOCSPCAConfigurationCollection interface [Security],CreateCAConfiguration method, IOCSPCAConfigurationCollection.CreateCAConfiguration, IOCSPCAConfigurationCollection::CreateCAConfiguration, certadm/IOCSPCAConfigurationCollection::CreateCAConfiguration, security.iocspcaconfigurationcollection_createcaconfiguration_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPCAConfigurationCollection.CreateCAConfiguration
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPCAConfigurationCollection::CreateCAConfiguration


## -description


The <b>CreateCAConfiguration</b> method creates a new <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) configuration and adds it to the configuration set.


## -parameters




### -param bstrIdentifier [in]

A string that contains a name for the new <a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a> object.


### -param varCACert [in]

An X.509 CA certificate.


### -param ppVal [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a> interface for the newly created object.


## -returns



<h3>C++</h3>
If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



<h3>VB</h3>
An 
<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 interface for the newly created object.



## -see-also




<a href="https://msdn.microsoft.com/4e232c34-b5ab-4269-903b-189aac5a8ddc">IOCSPCAConfigurationCollection</a>
 

 

