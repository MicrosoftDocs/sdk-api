---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetComponentType
title: IDvbComponentDescriptor::GetComponentType
author: windows-sdk-content
description: Gets the component type code for a Digital Video Broadcast (DVB) component descriptor.
old-location: mstv\idvbcomponentdescriptor_getcomponenttype.htm
old-project: mstv
ms.assetid: c7bf5e21-1c88-4b5e-b043-33a127fad65f
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetComponentType, GetComponentType method [Microsoft TV Technologies], GetComponentType method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetComponentType method, IDvbComponentDescriptor.GetComponentType, IDvbComponentDescriptor::GetComponentType, dvbsiparser/IDvbComponentDescriptor::GetComponentType, mstv.idvbcomponentdescriptor_getcomponenttype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbComponentDescriptor.GetComponentType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/0dee15ee-5b36-4454-8092-6b57ef5063ce">IDvbComponentDescriptor</a>
 

 

