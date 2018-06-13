---
UID: NF:sdoias.ISdoDictionaryOld.GetAttributeID
title: ISdoDictionaryOld::GetAttributeID
author: windows-sdk-content
description: The GetAttributeID method retrieves the ID for the specified attribute.
old-location: nps\SDO_isdodictionaryold_getattributeid.htm
old-project: Nps
ms.assetid: 30d2128e-6940-443d-b5e2-c9964d7edfa1
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetAttributeID, GetAttributeID method [Network Policy Server], GetAttributeID method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],GetAttributeID method, ISdoDictionaryOld.GetAttributeID, ISdoDictionaryOld::GetAttributeID, _sdo_isdodictionaryold_getattributeid, nps.SDO_isdodictionaryold_getattributeid, sdo.isdodictionaryold_getattributeid, sdoias/ISdoDictionaryOld::GetAttributeID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VENDORPROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoDictionaryOld.GetAttributeID
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISdoDictionaryOld::GetAttributeID


## -description


The 
<b>GetAttributeID</b> method retrieves the ID for the specified attribute.


## -parameters




### -param bstrAttributeName [in]

Specifies the name of the attribute. This name is either the Lightweight Directory Access Protocol (LDAP) name, or the display name for the attribute.


### -param pId [out]

Pointer to an 
<a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">ATTRIBUTEID</a> that receives the ID of the specified attribute.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method does not find the attribute, the return value is <b>DISP_E_MEMBERNOTFOUND</b>.

If the method fails, the return value is one of the following error codes.




## -see-also




<a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">ATTRIBUTEID</a>



<a href="https://msdn.microsoft.com/library/windows/desktop/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>



<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>
 

 

