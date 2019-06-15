---
UID: NF:sdoias.ISdoDictionaryOld.GetAttributeID
title: ISdoDictionaryOld::GetAttributeID (sdoias.h)
author: windows-sdk-content
description: The GetAttributeID method retrieves the ID for the specified attribute.
old-location: nps\SDO_isdodictionaryold_getattributeid.htm
tech.root: Nps
ms.assetid: 30d2128e-6940-443d-b5e2-c9964d7edfa1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAttributeID, GetAttributeID method [Network Policy Server], GetAttributeID method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],GetAttributeID method, ISdoDictionaryOld.GetAttributeID, ISdoDictionaryOld::GetAttributeID, _sdo_isdodictionaryold_getattributeid, nps.SDO_isdodictionaryold_getattributeid, sdo.isdodictionaryold_getattributeid, sdoias/ISdoDictionaryOld::GetAttributeID
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
req.lib: 
req.dll: Iassdo.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-_attributeid">ATTRIBUTEID</a> that receives the ID of the specified attribute.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method does not find the attribute, the return value is <b>DISP_E_MEMBERNOTFOUND</b>.

If the method fails, the return value is one of the following error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-_attributeid">ATTRIBUTEID</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold">ISdoDictionaryOld</a>
 

 

