---
UID: NF:certadm.IOCSPCAConfigurationCollection.DeleteCAConfiguration
title: IOCSPCAConfigurationCollection::DeleteCAConfiguration method
author: windows-driver-content
description: Removes a named certification authority (CA) configuration from the configuration set.
old-location: security\iocspcaconfigurationcollection_deletecaconfiguration_method.htm
old-project: SecCrypto
ms.assetid: 3733d98c-d262-4083-bac9-109720059f0b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeleteCAConfiguration method [Security], DeleteCAConfiguration method [Security], IOCSPCAConfigurationCollection interface, DeleteCAConfiguration,IOCSPCAConfigurationCollection.DeleteCAConfiguration, IOCSPCAConfigurationCollection, IOCSPCAConfigurationCollection interface [Security], DeleteCAConfiguration method, IOCSPCAConfigurationCollection::DeleteCAConfiguration, certadm/IOCSPCAConfigurationCollection::DeleteCAConfiguration, security.iocspcaconfigurationcollection_deletecaconfiguration_method
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CHANNEL_ENTRY_POINTS, *PCHANNEL_ENTRY_POINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certadm.dll
api_name:
-	IOCSPCAConfigurationCollection.DeleteCAConfiguration
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPCAConfigurationCollection::DeleteCAConfiguration method


## -description


The <b>DeleteCAConfiguration</b> method removes a named <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) configuration from the configuration set.


## -parameters




### -param bstrIdentifier [in]

A string that contains the name for the <a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a> object.


## -remarks



The <i>bstrIdentifier</i> value must be one previously set by the <a href="https://msdn.microsoft.com/d1c47402-77b1-4c43-8d57-20b9dd2682f7">CreateCAConfiguration</a> method.




## -see-also




<a href="https://msdn.microsoft.com/4e232c34-b5ab-4269-903b-189aac5a8ddc">IOCSPCAConfigurationCollection</a>
 

 

