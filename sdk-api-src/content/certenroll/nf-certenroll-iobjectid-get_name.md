---
UID: NF:certenroll.IObjectId.get_Name
title: IObjectId::get_Name (certenroll.h)
author: windows-sdk-content
description: Retrieves a CERTENROLL_OBJECTID value that contains an object identifier.
old-location: security\iobjectid_name_property.htm
tech.root: seccertenroll
ms.assetid: 3d3842a9-73b6-4fb8-83cf-ac65c5a09acb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IObjectId interface [Security],Name property, IObjectId.Name, IObjectId.get_Name, IObjectId::Name, IObjectId::get_Name, Name property [Security], Name property [Security],IObjectId interface, certenroll/IObjectId::Name, certenroll/IObjectId::get_Name, get_Name, security.iobjectid_name_property
ms.topic: method
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IObjectId.Name
 - IObjectId.get_Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectId::get_Name


## -description


The <b>Name</b> property retrieves a <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a> value that contains an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a>.

This property is read-only.


## -parameters


## -remarks



You must call any of the following methods before you can retrieve this property value:<ul>
<li>
<a href="https://msdn.microsoft.com/ba8c1f11-9380-43a9-b444-b0fff114a176">InitializeFromAlgorithmName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dce84308-aecc-4841-88da-e948313b90b3">InitializeFromName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2bb2ee69-02c3-41b9-a67b-036c7154a44e">InitializeFromValue</a>
</li>
</ul>


You can also retrieve the following property values:<ul>
<li>
<a href="https://msdn.microsoft.com/9360f652-afeb-4f30-a423-402f397b9255">FriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb681a-f31b-4d31-ae56-25efd2af2b2c">Value</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectID</a>
 

 

