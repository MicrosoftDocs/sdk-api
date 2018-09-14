---
UID: NE:sdoias._NTEVENTLOGPROPERTIES
title: "_NTEVENTLOGPROPERTIES"
author: windows-sdk-content
description: The values of the NTEVENTLOGPROPERTIES enumeration type enumerate what types of events should be logged in the NT Event Log.
old-location: nps\SDO_nteventlogproperties.htm
tech.root: Nps
ms.assetid: 5b52eae6-4a72-4935-8a82-6e7747ce942e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NTEVENTLOGPROPERTIES, NTEVENTLOGPROPERTIES enumeration [Network Policy Server], PROPERTY_EVENTLOG_LOG_APPLICATION_EVENTS, PROPERTY_EVENTLOG_LOG_DEBUG, PROPERTY_EVENTLOG_LOG_MALFORMED, _NTEVENTLOGPROPERTIES, _sdo_nteventlogproperties, nps.SDO_nteventlogproperties, sdo.nteventlogproperties, sdoias/NTEVENTLOGPROPERTIES, sdoias/PROPERTY_EVENTLOG_LOG_APPLICATION_EVENTS, sdoias/PROPERTY_EVENTLOG_LOG_DEBUG, sdoias/PROPERTY_EVENTLOG_LOG_MALFORMED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - NTEVENTLOGPROPERTIES
product: Windows
targetos: Windows
req.typenames: NTEVENTLOGPROPERTIES
req.redist: 
---

# _NTEVENTLOGPROPERTIES enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008. The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The values of the 
<b>NTEVENTLOGPROPERTIES</b> enumeration type enumerate what types of events should be logged in the NT Event Log.


## -enum-fields




### -field PROPERTY_EVENTLOG_LOG_APPLICATION_EVENTS

Specifies how the reporting of NPS Error events occurs in the Windows event log. In Windows XP, there is no UI element that corresponds to this property


### -field PROPERTY_EVENTLOG_LOG_MALFORMED

Specifies whether discarded and rejected packets are logged.


### -field PROPERTY_EVENTLOG_LOG_DEBUG

Specifies whether successful authentications are logged.

