---
UID: NF:imapi.IDiscMaster.SetActiveDiscMasterFormat
title: IDiscMaster::SetActiveDiscMasterFormat (imapi.h)
description: Sets the currently active disc recorder format. The active format specifies both the structure of the staged image file content (audio/data) and the COM interface that must be used to manipulate that staged image.
helpviewer_keywords: ["IDiscMaster interface [IMAPI]","SetActiveDiscMasterFormat method","IDiscMaster.SetActiveDiscMasterFormat","IDiscMaster::SetActiveDiscMasterFormat","SetActiveDiscMasterFormat","SetActiveDiscMasterFormat method [IMAPI]","SetActiveDiscMasterFormat method [IMAPI]","IDiscMaster interface","_win32_idiscmaster_setactivediscmasterformat","base.idiscmaster_setactivediscmasterformat","imapi.idiscmaster_setactivediscmasterformat","imapi/IDiscMaster::SetActiveDiscMasterFormat"]
old-location: imapi\idiscmaster_setactivediscmasterformat.htm
tech.root: imapi
ms.assetid: fcc2840b-d302-4cd6-b576-1826c83b711e
ms.date: 12/05/2018
ms.keywords: IDiscMaster interface [IMAPI],SetActiveDiscMasterFormat method, IDiscMaster.SetActiveDiscMasterFormat, IDiscMaster::SetActiveDiscMasterFormat, SetActiveDiscMasterFormat, SetActiveDiscMasterFormat method [IMAPI], SetActiveDiscMasterFormat method [IMAPI],IDiscMaster interface, _win32_idiscmaster_setactivediscmasterformat, base.idiscmaster_setactivediscmasterformat, imapi.idiscmaster_setactivediscmasterformat, imapi/IDiscMaster::SetActiveDiscMasterFormat
req.header: imapi.h
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
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscMaster::SetActiveDiscMasterFormat
 - imapi/IDiscMaster::SetActiveDiscMasterFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscMaster.SetActiveDiscMasterFormat
---

# IDiscMaster::SetActiveDiscMasterFormat


## -description

Sets the currently active disc recorder format. The active format specifies both the structure of the staged image file content (audio/data) and the COM interface that must be used to manipulate that staged image.

## -parameters

### -param riid [in]

IID of the currently active format.

### -param ppUnk [out]

Pointer to the COM interface for the new disc format.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

A successful call to this method clears the contents of the currently staged image. In addition, it may change the list of supported disc recorders. This is because not all recorders support all formats. Changes to the recorder list are announced with 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifypnpactivity">IDiscMasterProgressEvents::NotifyPnPActivity</a>. If the currently selected recorder is not a member of the new set of supported devices, then there will no longer be an active recorder (similar to the state after the first call to 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-open">Open</a>). In this case, the application must select a new active recorder before initiating a burn.

<b>MSDiscMasterObj</b> supports only the following IIDs: IID_IRedbookDiscMaster (<a href="/windows/desktop/api/imapi/nn-imapi-iredbookdiscmaster">IRedbookDiscMaster</a>) and IID_IJolietDiscMaster (<a href="/windows/desktop/api/imapi/nn-imapi-ijolietdiscmaster">IJolietDiscMaster</a>). If there is no format set, the default is Joliet format. It is the responsibility of every application to select a format master through the use of 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-enumdiscmasterformats">EnumDiscMasterFormats</a> and this method.

<div class="alert"><b>Note</b>  A call to this method may change the list of available recorders. See the Remarks section of 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-enumdiscrecorders">EnumDiscRecorders</a> for more information.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>