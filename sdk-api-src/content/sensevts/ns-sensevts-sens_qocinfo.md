---
UID: NS:sensevts.SENS_QOCINFO
title: SENS_QOCINFO (sensevts.h)
description: The SENS_QOCINFO structure is used by the ISensNetwork::ConnectionMade method. This structure contains Quality of Connection information to the sink object in an application that subscribes to SENS.
helpviewer_keywords: ["*LPSENS_QOCINFO","SENS_QOCINFO","SENS_QOCINFO structure [SENS]","_zaw_sens_qocinfo","sens.sens_qocinfo","sensevts/SENS_QOCINFO","syncmgr.sens_qocinfo"]
old-location: sens\sens_qocinfo.htm
tech.root: Sens
ms.assetid: 33f5e790-1100-46a9-a90c-3fc51379c175
ms.date: 12/05/2018
ms.keywords: '*LPSENS_QOCINFO, SENS_QOCINFO, SENS_QOCINFO structure [SENS], _zaw_sens_qocinfo, sens.sens_qocinfo, sensevts/SENS_QOCINFO, syncmgr.sens_qocinfo'
req.header: sensevts.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SENS_QOCINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SENS_QOCINFO
 - sensevts/SENS_QOCINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sensevts.h
api_name:
 - SENS_QOCINFO
---

# SENS_QOCINFO structure


## -description

The 
<b>SENS_QOCINFO</b> structure is used by the 
<a href="/windows/desktop/api/sensevts/nf-sensevts-isensnetwork-connectionmade">ISensNetwork::ConnectionMade</a> method. This structure contains Quality of Connection information to the sink object in an application that subscribes to SENS.

## -struct-fields

### -field dwSize

This member contains the actual size of the structure that was filled in.

### -field dwFlags

Speed of connection. Flag bits indicate whether the connection is slow, medium, fast.

### -field dwOutSpeed

Speed of data sent to the destination in bits per second.

### -field dwInSpeed

Speed of data coming in from the destination in bits per second.

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isensnetwork-connectionmade">ISensNetwork::ConnectionMade</a>