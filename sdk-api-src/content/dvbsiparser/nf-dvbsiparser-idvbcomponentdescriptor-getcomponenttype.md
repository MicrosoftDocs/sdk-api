---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetComponentType
title: IDvbComponentDescriptor::GetComponentType (dvbsiparser.h)
description: Gets the component type code for a Digital Video Broadcast (DVB) component descriptor.helpviewer_keywords: ["GetComponentType","GetComponentType method [Microsoft TV Technologies]","GetComponentType method [Microsoft TV Technologies]","IDvbComponentDescriptor interface","IDvbComponentDescriptor interface [Microsoft TV Technologies]","GetComponentType method","IDvbComponentDescriptor.GetComponentType","IDvbComponentDescriptor::GetComponentType","dvbsiparser/IDvbComponentDescriptor::GetComponentType","mstv.idvbcomponentdescriptor_getcomponenttype"]
old-location: mstv\idvbcomponentdescriptor_getcomponenttype.htm
tech.root: mstv
ms.assetid: c7bf5e21-1c88-4b5e-b043-33a127fad65f
ms.date: 12/05/2018
ms.keywords: GetComponentType, GetComponentType method [Microsoft TV Technologies], GetComponentType method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetComponentType method, IDvbComponentDescriptor.GetComponentType, IDvbComponentDescriptor::GetComponentType, dvbsiparser/IDvbComponentDescriptor::GetComponentType, mstv.idvbcomponentdescriptor_getcomponenttype
f1_keywords:
- dvbsiparser/IDvbComponentDescriptor.GetComponentType
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IDvbComponentDescriptor.GetComponentType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbComponentDescriptor::GetComponentType


## -description


Gets the component type code for a Digital Video Broadcast (DVB) component descriptor.


## -parameters




### -param pbVal [out]

Receives the component type code. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of component types associated with the value returned in the <i>pbVal</i>  parameter, see Table 26 in Section 6.2.9 of the DVB standards document,  
      <i>Digital Video Broadcasting Specification for Service Information (SI) in DVB systems</i>. (This resource may not be available in some languages 

and countries.)




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcomponentdescriptor">IDvbComponentDescriptor</a>
 

 

