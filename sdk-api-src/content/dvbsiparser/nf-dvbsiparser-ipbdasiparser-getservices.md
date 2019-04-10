---
UID: NF:dvbsiparser.IPBDASiParser.GetServices
title: IPBDASiParser::GetServices (dvbsiparser.h)
author: windows-sdk-content
description: Retrieves a list of services from the program and system information protocol (PSIP) tables in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbdasiparser_getservices.htm
tech.root: mstv
ms.assetid: 0d6848f2-6fcd-4e7c-b1fc-b8f56e6c65b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetServices, GetServices method [Microsoft TV Technologies], GetServices method [Microsoft TV Technologies],IPBDASiParser interface, IPBDASiParser interface [Microsoft TV Technologies],GetServices method, IPBDASiParser.GetServices, IPBDASiParser::GetServices, dshow.ipbdasiparser_getservices, dvbsiparser/IPBDASiParser::GetServices, mstv.ipbdasiparser_getservices
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
 - IPBDASiParser.GetServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPBDASiParser::GetServices


## -description


Retrieves a list of services from the  program and system information protocol (PSIP) tables in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -parameters




### -param dwSize [in]

Size of the buffer that receives the service list, in bytes.


### -param pBuffer [in]

Receives the buffer for services.


### -param ppServices [out]

Receives an <a href="https://msdn.microsoft.com/8d2d62cd-9f62-45d3-8b98-74bb8863c6d6">IPBDA_Services</a> interface pointer.  The caller must release this interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a1cc25ec-b519-4c24-ba85-f2c240749fbd">IPBDASiParser</a>



<a href="https://msdn.microsoft.com/8d2d62cd-9f62-45d3-8b98-74bb8863c6d6">IPBDA_Services</a>
 

 

