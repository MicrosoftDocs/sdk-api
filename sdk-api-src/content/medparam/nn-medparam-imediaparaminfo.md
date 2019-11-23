---
UID: NN:medparam.IMediaParamInfo
title: IMediaParamInfo (medparam.h)

description: The IMediaParamInfo interface retrieves information about the parameters that an object supports. The set of parameters that an object supports will not change over the lifetime of an application. To set parameter values, use the IMediaParams interface.
old-location: dshow\imediaparaminfo.htm
tech.root: DirectShow
ms.assetid: 80c7da71-7898-4bda-a181-09ad8906532a

ms.date: 12/05/2018
ms.keywords: IMediaParamInfo, IMediaParamInfo interface [DirectShow], IMediaParamInfo interface [DirectShow],described, IMediaParamInfoInterface, dshow.imediaparaminfo, medparam/IMediaParamInfo
ms.topic: interface
f1_keywords: 
 - "medparam/IMediaParamInfo"
dev_langs:
 - c++
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParamInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaParamInfo interface


## -description



The <code>IMediaParamInfo</code> interface retrieves information about the parameters that an object supports. The set of parameters that an object supports will not change over the lifetime of an application. To set parameter values, use the <a href="https://docs.microsoft.com/windows/desktop/api/medparam/nn-medparam-imediaparams">IMediaParams</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaParamInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaParamInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaParamInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getcurrenttimeformat">GetCurrentTimeFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current time format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getnumtimeformats">GetNumTimeFormats</a>
</td>
<td align="left" width="63%">
Retrieves the number of time formats that the object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getparamcount">GetParamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of parameters that the object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getparaminfo">GetParamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getparamtext">GetParamText</a>
</td>
<td align="left" width="63%">
Retrieves an array of text strings that describe the parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat">GetSupportedTimeFormat</a>
</td>
<td align="left" width="63%">
Retrieves a supported time format.

</td>
</tr>
</table> 

