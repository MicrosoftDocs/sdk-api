---
UID: NF:certenroll.IObjectId.put_FriendlyName
title: IObjectId::put_FriendlyName
author: windows-driver-content
description: Specifies and retrieves a display name for the object identifier.
old-location: security\iobjectid_friendlyname_property.htm
old-project: SecCertEnroll
ms.assetid: 9360f652-afeb-4f30-a423-402f397b9255
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: FriendlyName property [Security], FriendlyName property [Security],IObjectId interface, IObjectId interface [Security],FriendlyName property, IObjectId.FriendlyName, IObjectId.put_FriendlyName, IObjectId::FriendlyName, IObjectId::get_FriendlyName, IObjectId::put_FriendlyName, certenroll/IObjectId::FriendlyName, certenroll/IObjectId::get_FriendlyName, certenroll/IObjectId::put_FriendlyName, put_FriendlyName, security.iobjectid_friendlyname_property
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IObjectId.FriendlyName
-	IObjectId.get_FriendlyName
-	IObjectId.put_FriendlyName
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IObjectId::put_FriendlyName


## -description


The <b>FriendlyName</b> property specifies and retrieves a display name for the object identifier. The display name exists until another name is specified or the object lifetime has ended. This property is web enabled for output.

This property is read/write.


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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a>
 

 

