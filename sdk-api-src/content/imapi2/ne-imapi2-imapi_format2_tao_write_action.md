---
UID: NE:imapi2._IMAPI_FORMAT2_TAO_WRITE_ACTION
title: IMAPI_FORMAT2_TAO_WRITE_ACTION (imapi2.h)
author: windows-sdk-content
description: Defines values that indicate the current state of the write operation when using the IDiscFormat2TrackAtOnceEventArgs interface.
old-location: imapi\imapi_format2_tao_write_action.htm
tech.root: imapi
ms.assetid: 82d5b842-1bc1-41c7-acb3-faf9986329c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIMAPI_FORMAT2_TAO_WRITE_ACTION, IMAPI_FORMAT2_TAO_WRITE_ACTION, IMAPI_FORMAT2_TAO_WRITE_ACTION enumeration [IMAPI], IMAPI_FORMAT2_TAO_WRITE_ACTION_FINISHING, IMAPI_FORMAT2_TAO_WRITE_ACTION_PREPARING, IMAPI_FORMAT2_TAO_WRITE_ACTION_UNKNOWN, IMAPI_FORMAT2_TAO_WRITE_ACTION_WRITING, PIMAPI_FORMAT2_TAO_WRITE_ACTION, PIMAPI_FORMAT2_TAO_WRITE_ACTION enumeration pointer [IMAPI], imapi.imapi_format2_tao_write_action, imapi2/IMAPI_FORMAT2_TAO_WRITE_ACTION, imapi2/IMAPI_FORMAT2_TAO_WRITE_ACTION_FINISHING, imapi2/IMAPI_FORMAT2_TAO_WRITE_ACTION_PREPARING, imapi2/IMAPI_FORMAT2_TAO_WRITE_ACTION_UNKNOWN, imapi2/IMAPI_FORMAT2_TAO_WRITE_ACTION_WRITING, imapi2/PIMAPI_FORMAT2_TAO_WRITE_ACTION"
ms.topic: enum
f1_keywords: 
 - "imapi2/IMAPI_FORMAT2_TAO_WRITE_ACTION"
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IMAPI_FORMAT2_TAO_WRITE_ACTION
targetos: Windows
req.typenames: IMAPI_FORMAT2_TAO_WRITE_ACTION, *PIMAPI_FORMAT2_TAO_WRITE_ACTION
req.redist: 
ms.custom: 19H1
---

# IMAPI_FORMAT2_TAO_WRITE_ACTION enumeration


## -description


Defines values that indicate the current state of the write operation when using the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs">IDiscFormat2TrackAtOnceEventArgs</a> interface.


## -enum-fields




### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_UNKNOWN

Indicates an unknown state.


### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_PREPARING

Preparing to write the track.


### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_WRITING

Writing the track.


### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_FINISHING

Closing the track or closing the session.


### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_VERIFYING




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2trackatonceevents-update">DDiscFormat2TrackAtOnceEvents::Update</a>
 

 

