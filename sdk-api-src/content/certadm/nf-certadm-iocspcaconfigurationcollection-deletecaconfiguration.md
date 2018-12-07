---
UID: NF:certadm.IOCSPCAConfigurationCollection.DeleteCAConfiguration
title: IOCSPCAConfigurationCollection::DeleteCAConfiguration
author: windows-sdk-content
description: Removes a named certification authority (CA) configuration from the configuration set.
old-location: security\iocspcaconfigurationcollection_deletecaconfiguration_method.htm
tech.root: seccrypto
ms.assetid: 3733d98c-d262-4083-bac9-109720059f0b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteCAConfiguration, DeleteCAConfiguration method [Security], DeleteCAConfiguration method [Security],IOCSPCAConfigurationCollection interface, IOCSPCAConfigurationCollection interface [Security],DeleteCAConfiguration method, IOCSPCAConfigurationCollection.DeleteCAConfiguration, IOCSPCAConfigurationCollection::DeleteCAConfiguration, certadm/IOCSPCAConfigurationCollection::DeleteCAConfiguration, security.iocspcaconfigurationcollection_deletecaconfiguration_method
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
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPCAConfigurationCollection.DeleteCAConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPCAConfigurationCollection::DeleteCAConfiguration


## -description


The <b>DeleteCAConfiguration</b> method removes a named <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) configuration from the configuration set.


## -parameters




### -param bstrIdentifier [in]

A string that contains the name for the <a href="https://msdn.microsoft.com/en-us/library/Aa386328(v=VS.85).aspx">IOCSPCAConfiguration</a> object.


## -remarks



The <i>bstrIdentifier</i> value must be one previously set by the <a href="https://msdn.microsoft.com/en-us/library/Aa386335(v=VS.85).aspx">CreateCAConfiguration</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386330(v=VS.85).aspx">IOCSPCAConfigurationCollection</a>
 

 

