---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetLogoCharW
title: IIsdbLogoTransmissionDescriptor::GetLogoCharW
author: windows-sdk-content
description: Gets the character string for a simple logo from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
old-location: mstv\iisdblogotransmissiondescriptor_getlogocharw.htm
old-project: mstv
ms.assetid: bb4ba9f1-f633-4cb4-adc4-6671bb5fc239
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetLogoCharW, GetLogoCharW method [Microsoft TV Technologies], GetLogoCharW method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetLogoCharW method, IIsdbLogoTransmissionDescriptor.GetLogoCharW, IIsdbLogoTransmissionDescriptor::GetLogoCharW, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoCharW, mstv.iisdblogotransmissiondescriptor_getlogocharw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IIsdbLogoTransmissionDescriptor.GetLogoCharW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbLogoTransmissionDescriptor::GetLogoCharW


## -description


 Gets the character string for a simple logo from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor. 


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrChar [out]

Pointer to a buffer that receives the logo text. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9c0930f6-6c05-48c9-91e4-2abdd3355a32">IIsdbLogoTransmissionDescriptor</a>
 

 

