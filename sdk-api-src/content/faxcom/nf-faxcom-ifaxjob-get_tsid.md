---
UID: NF:faxcom.IFaxJob.get_Tsid
title: IFaxJob::get_Tsid (faxcom.h)
description: The IFaxJob::get_Tsid property is a null-terminated string that contains the transmitting station identifier (TSID)) associated with the fax job.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","Tsid property","IFaxJob.Tsid","IFaxJob.get_Tsid","IFaxJob::Tsid","IFaxJob::get_Tsid","Tsid property [Fax Service]","Tsid property [Fax Service]","IFaxJob interface","_mfax_ifaxjob_get_tsid","fax._mfax_ifaxjob_get_tsid","fax._mfax_ifaxjob_mfax_ifaxjob_get_tsid_cpp","faxcom/IFaxJob::Tsid","faxcom/IFaxJob::get_Tsid","get_Tsid"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4zz8.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],Tsid property, IFaxJob.Tsid, IFaxJob.get_Tsid, IFaxJob::Tsid, IFaxJob::get_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_tsid, fax._mfax_ifaxjob_get_tsid, fax._mfax_ifaxjob_mfax_ifaxjob_get_tsid_cpp, faxcom/IFaxJob::Tsid, faxcom/IFaxJob::get_Tsid, get_Tsid
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
 - IFaxJob::get_Tsid
 - faxcom/IFaxJob::get_Tsid
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
 - IFaxJob.Tsid
 - IFaxJob.get_Tsid
---

# IFaxJob::get_Tsid


## -description

The <b>IFaxJob::get_Tsid</b> property is a null-terminated string that contains the 
transmitting station identifier (TSID)) associated with the fax job.

This property is read-only.

## -parameters

## -remarks

If the TSID is not available, <b>IFaxJob::get_Tsid</b> is an empty string. 

You can use the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-usedevicetsid-vb">UseDeviceTsid</a> property to determine if the fax server is configured to permit user-specified TSIDs. 

Note that the T.30 specification of the International Telecommunication Union (ITU) restricts the value of a TSID to 20 ASCII characters. If a fax client application specifies a TSID that contains non-ASCII characters, the fax service removes them. If the TSID exceeds 20 characters, the service truncates the extra characters. 

<b>IFaxJob::get_Tsid</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-usedevicetsid-vb">UseDeviceTsid</a>