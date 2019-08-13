---
UID: NF:sdoias.ISdoDictionaryOld.GetAttributeInfo
title: ISdoDictionaryOld::GetAttributeInfo (sdoias.h)
author: windows-sdk-content
description: The GetAttributeInfo retrieves information for the specified attribute.
old-location: nps\SDO_isdodictionaryold_getattributeinfo.htm
tech.root: Nps
ms.assetid: 80535d3c-17bb-482b-b5bb-7d747f238b62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAttributeInfo, GetAttributeInfo method [Network Policy Server], GetAttributeInfo method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],GetAttributeInfo method, ISdoDictionaryOld.GetAttributeInfo, ISdoDictionaryOld::GetAttributeInfo, _sdo_isdodictionaryold_getattributeinfo, nps.SDO_isdodictionaryold_getattributeinfo, sdo.isdodictionaryold_getattributeinfo, sdoias/ISdoDictionaryOld::GetAttributeInfo
ms.topic: method
f1_keywords:
- sdoias/ISdoDictionaryOld.GetAttributeInfo
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
- ISdoDictionaryOld.GetAttributeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISdoDictionaryOld::GetAttributeInfo


## -description


The <b>GetAttributeInfo</b> 
    retrieves information for the specified attribute.


## -parameters




### -param Id [in]

Specifies the ID for the attribute.


### -param pInfoIDs [in]

Pointer to an array of information IDs. This pointer cannot be <b>NULL</b>.


### -param pInfoValues [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> of 
      information values.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Although Server Data Objects (SDO) exposes this method, you do not need it in order to use SDO. The use of 
    this method is discouraged.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-attributeinfo">ATTRIBUTEINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold">ISdoDictionaryOld</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>
 

 

