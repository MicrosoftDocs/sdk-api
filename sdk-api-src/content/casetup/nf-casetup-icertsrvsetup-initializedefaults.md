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

# ICertSrvSetup::InitializeDefaults


## -description


The <b>InitializeDefaults</b> method initializes a <b>CCertSrvSetup</b> object with default values to enable installation of the Certification Authority role. To install a CA role, this method must be called before using the <b>CCertSrvSetup</b> object. For information about default values, see <a href="https://msdn.microsoft.com/2245ad2f-89ca-4478-91d0-cbd7a0648479">CASetupProperty</a>.


## -parameters




### -param bServer [in]

A value that indicates whether a CA will be installed on the computer. A <b>VARIANT_TRUE</b> value indicates that the role will be installed. Neither the Certification Authority nor Certification Authority Web Enrollment roles can be previously installed on the computer.


### -param bClient [in]

A value that indicates whether a Certification Authority Web Enrollment role will be installed on the computer. A <b>VARIANT_TRUE</b> value indicates that the role will be installed. This role cannot be previously installed on the computer.


## -remarks



If the policy statement file "CAPolicy.inf" is installed, <b>InitializeDefaults</b> processes it.




## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

