---
UID: NF:faxcomex.IFaxOutgoingArchive.put_UseArchive
title: IFaxOutgoingArchive::put_UseArchive (faxcomex.h)
description: The IFaxOutgoingArchive::get_UseArchive property is a Boolean value that indicates whether the fax service archives outbound fax messages. (Put)
helpviewer_keywords: ["IFaxOutgoingArchive interface [Fax Service]","UseArchive property","IFaxOutgoingArchive.UseArchive","IFaxOutgoingArchive.get_UseArchive","IFaxOutgoingArchive.put_UseArchive","IFaxOutgoingArchive::UseArchive","IFaxOutgoingArchive::get_UseArchive","IFaxOutgoingArchive::put_UseArchive","UseArchive property [Fax Service]","UseArchive property [Fax Service]","IFaxOutgoingArchive interface","_mfax_faxoutgoingarchive.usearchive","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_usearchive_cpp","fax._mfax_faxoutgoingarchive_usearchive","faxcomex/IFaxOutgoingArchive::UseArchive","faxcomex/IFaxOutgoingArchive::get_UseArchive","faxcomex/IFaxOutgoingArchive::put_UseArchive","put_UseArchive"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_usearchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4pk5.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],UseArchive property, IFaxOutgoingArchive.UseArchive, IFaxOutgoingArchive.get_UseArchive, IFaxOutgoingArchive.put_UseArchive, IFaxOutgoingArchive::UseArchive, IFaxOutgoingArchive::get_UseArchive, IFaxOutgoingArchive::put_UseArchive, UseArchive property [Fax Service], UseArchive property [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.usearchive, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_usearchive_cpp, fax._mfax_faxoutgoingarchive_usearchive, faxcomex/IFaxOutgoingArchive::UseArchive, faxcomex/IFaxOutgoingArchive::get_UseArchive, faxcomex/IFaxOutgoingArchive::put_UseArchive, put_UseArchive
req.header: faxcomex.h
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
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutgoingArchive::put_UseArchive
 - faxcomex/IFaxOutgoingArchive::put_UseArchive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingArchive.UseArchive
 - IFaxOutgoingArchive.get_UseArchive
 - IFaxOutgoingArchive.put_UseArchive
 - IFaxOutgoingArchive.get_UseArchive
 - IFaxOutgoingArchive.put_UseArchive
---

# IFaxOutgoingArchive::put_UseArchive


## -description

The <b>IFaxOutgoingArchive::get_UseArchive</b> property is a Boolean value that indicates whether the fax service archives outbound fax messages. If this parameter is equal to <b>TRUE</b>, the fax service archives outbound fax messages. If this parameter is equal to <b>FALSE</b>, the fax service does not archive outbound faxes.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-usearchive-vb">IFaxConfiguration::put_UseArchive</a>   or <b>IFaxConfiguration::get_UseArchive</b> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-outgoing-archive">Visual Basic Example</a>
