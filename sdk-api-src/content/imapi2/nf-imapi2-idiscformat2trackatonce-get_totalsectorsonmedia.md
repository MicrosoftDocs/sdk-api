---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_TotalSectorsOnMedia
title: IDiscFormat2TrackAtOnce::get_TotalSectorsOnMedia (imapi2.h)
description: Retrieves the total sectors available on the media if writing one continuous audio track.helpviewer_keywords: ["IDiscFormat2TrackAtOnce interface [IMAPI]","get_TotalSectorsOnMedia method","IDiscFormat2TrackAtOnce.get_TotalSectorsOnMedia","IDiscFormat2TrackAtOnce::get_TotalSectorsOnMedia","get_TotalSectorsOnMedia","get_TotalSectorsOnMedia method [IMAPI]","get_TotalSectorsOnMedia method [IMAPI]","IDiscFormat2TrackAtOnce interface","imapi.idiscformat2trackatonce_get_totalsectorsonmedia","imapi2/IDiscFormat2TrackAtOnce::get_TotalSectorsOnMedia"]
old-location: imapi\idiscformat2trackatonce_get_totalsectorsonmedia.htm
tech.root: imapi
ms.assetid: 86af52be-d1ea-4ccb-b1b4-e301d70cac53
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_TotalSectorsOnMedia method, IDiscFormat2TrackAtOnce.get_TotalSectorsOnMedia, IDiscFormat2TrackAtOnce::get_TotalSectorsOnMedia, get_TotalSectorsOnMedia, get_TotalSectorsOnMedia method [IMAPI], get_TotalSectorsOnMedia method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_totalsectorsonmedia, imapi2/IDiscFormat2TrackAtOnce::get_TotalSectorsOnMedia
f1_keywords:
- imapi2/IDiscFormat2TrackAtOnce.get_TotalSectorsOnMedia
dev_langs:
- c++
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
- COM
api_location:
- imapi2.h
api_name:
- IDiscFormat2TrackAtOnce.get_TotalSectorsOnMedia
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscFormat2TrackAtOnce::get_TotalSectorsOnMedia


## -description


Retrieves the total sectors available on the media if writing one continuous audio track.


## -parameters




### -param value [out]

Number of all sectors on the media that can be used for audio if one continuous audio track was recorded.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The media is not prepared (IDiscFormat2TrackAtOnce::PrepareMedia has not been called).

Value: 0xC0AA0502

</td>
</tr>
</table>
 




## -remarks



This property can be retrieved at any time; however, during writing, the value  is cached.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_freesectorsonmedia">IDiscFormat2Data::get_FreeSectorsOnMedia</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_totalsectorsonmedia">IDiscFormat2Data::get_TotalSectorsOnMedia</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_freesectorsonmedia">IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_usedsectorsonmedia">IDiscFormat2TrackAtOnce::get_UsedSectorsOnMedia</a>
 

 

