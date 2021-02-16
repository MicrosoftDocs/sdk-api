---
UID: NF:certenroll.IObjectId.get_Name
title: IObjectId::get_Name (certenroll.h)
description: Retrieves a CERTENROLL_OBJECTID value that contains an object identifier.
helpviewer_keywords: ["IObjectId interface [Security]","Name property","IObjectId.Name","IObjectId.get_Name","IObjectId::Name","IObjectId::get_Name","Name property [Security]","Name property [Security]","IObjectId interface","certenroll/IObjectId::Name","certenroll/IObjectId::get_Name","get_Name","security.iobjectid_name_property"]
old-location: security\iobjectid_name_property.htm
tech.root: security
ms.assetid: 3d3842a9-73b6-4fb8-83cf-ac65c5a09acb
ms.date: 12/05/2018
ms.keywords: IObjectId interface [Security],Name property, IObjectId.Name, IObjectId.get_Name, IObjectId::Name, IObjectId::get_Name, Name property [Security], Name property [Security],IObjectId interface, certenroll/IObjectId::Name, certenroll/IObjectId::get_Name, get_Name, security.iobjectid_name_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectId::get_Name
 - certenroll/IObjectId::get_Name
dev_langs:
 - c++
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
---

# IObjectId::get_Name


## -description

The <b>Name</b> property retrieves a <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a> value that contains an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a>.

This property is read-only.

## -parameters

## -remarks

You must call any of the following methods before you can retrieve this property value:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromname">InitializeFromName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromvalue">InitializeFromValue</a>
</li>
</ul>


You can also retrieve the following property values:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_friendlyname">FriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_value">Value</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectID</a>