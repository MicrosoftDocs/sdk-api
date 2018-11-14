---
UID: NF:sdoias.ISdoDictionaryOld.GetAttributeInfo
title: ISdoDictionaryOld::GetAttributeInfo
author: windows-sdk-content
description: The GetAttributeInfo retrieves information for the specified attribute.
old-location: nps\SDO_isdodictionaryold_getattributeinfo.htm
tech.root: Nps
ms.assetid: 80535d3c-17bb-482b-b5bb-7d747f238b62
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetAttributeInfo, GetAttributeInfo method [Network Policy Server], GetAttributeInfo method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],GetAttributeInfo method, ISdoDictionaryOld.GetAttributeInfo, ISdoDictionaryOld::GetAttributeInfo, _sdo_isdodictionaryold_getattributeinfo, nps.SDO_isdodictionaryold_getattributeinfo, sdo.isdodictionaryold_getattributeinfo, sdoias/ISdoDictionaryOld::GetAttributeInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISdoDictionaryOld.GetAttributeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sdoias.h
: 
- ISdoDictionaryOld.GetAttributeInfo
: 
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

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> of 
      information values.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Although Server Data Objects (SDO) exposes this method, you do not need it in order to use SDO. The use of 
    this method is discouraged.




## -see-also




<a href="https://msdn.microsoft.com/84ed435c-c6e8-41e7-9a5f-acd78fce4a10">ATTRIBUTEINFO</a>



<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a>
 

 

