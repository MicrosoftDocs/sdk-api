---
UID: NF:faxcom.IFaxTiff.get_RawReceiveTime
title: IFaxTiff::get_RawReceiveTime (faxcom.h)
description: Retrieves the RawReceiveTime property for a FaxTiff object.
helpviewer_keywords: ["IFaxTiff interface [Fax Service]","RawReceiveTime property","IFaxTiff.RawReceiveTime","IFaxTiff.get_RawReceiveTime","IFaxTiff::RawReceiveTime","IFaxTiff::get_RawReceiveTime","RawReceiveTime property [Fax Service]","RawReceiveTime property [Fax Service]","IFaxTiff interface","_mfax_ifaxtiff_get_rawreceivetime","fax._mfax_ifaxtiff_get_rawreceivetime","fax._mfax_ifaxtiff_mfax_ifaxtiff_get_rawreceivetime_cpp","faxcom/IFaxTiff::RawReceiveTime","faxcom/IFaxTiff::get_RawReceiveTime","get_RawReceiveTime"]
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_rawreceivetime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9usl.htm
ms.date: 12/05/2018
ms.keywords: IFaxTiff interface [Fax Service],RawReceiveTime property, IFaxTiff.RawReceiveTime, IFaxTiff.get_RawReceiveTime, IFaxTiff::RawReceiveTime, IFaxTiff::get_RawReceiveTime, RawReceiveTime property [Fax Service], RawReceiveTime property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_rawreceivetime, fax._mfax_ifaxtiff_get_rawreceivetime, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_rawreceivetime_cpp, faxcom/IFaxTiff::RawReceiveTime, faxcom/IFaxTiff::get_RawReceiveTime, get_RawReceiveTime
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxTiff::get_RawReceiveTime
 - faxcom/IFaxTiff::get_RawReceiveTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxTiff.RawReceiveTime
 - IFaxTiff.get_RawReceiveTime
---

# IFaxTiff::get_RawReceiveTime


## -description

Retrieves the <b>RawReceiveTime</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object. The <b>RawReceiveTime</b> property is the time at which reception began for an inbound fax file, expressed in Coordinated Universal Time (UTC). This property can also be the time at which reception or transmission began for an archived file.

This property is read-only.

## -parameters

## -remarks

A fax client application must  set the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">Image</a> property before retrieving another property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

The <b>get_RawReceiveTime</b> method sets the <i>pVal</i> parameter to the local time at which the fax job started receiving or transmitting the fax file. 

The <b>RawReceiveTime</b> property contains the local time at which the fax job started receiving or transmitting the fax file. 

The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-receivetime-vb">get_ReceiveTime</a> method returns the time in a formatted string.

The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-receivetime-vb">ReceiveTime</a> property contains the time in a formatted string.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">IFaxTiff::get_Image</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-receivetime-vb">IFaxTiff::get_ReceiveTime</a>