---
UID: NF:wtsprotocol.IWTSProtocolConnection.QueryProperty
title: IWTSProtocolConnection::QueryProperty (wtsprotocol.h)
description: IWTSProtocolConnection::QueryProperty is no longer available. Instead, use IWRdsProtocolConnection::QueryProperty.
helpviewer_keywords: ["IWTSProtocolConnection interface [Remote Desktop Services]","QueryProperty method","IWTSProtocolConnection.QueryProperty","IWTSProtocolConnection::QueryProperty","PROPERTY_DYNAMIC_TIME_ZONE_INFORMATION","QueryProperty","QueryProperty method [Remote Desktop Services]","QueryProperty method [Remote Desktop Services]","IWTSProtocolConnection interface","WTS_QUERY_ALLOWED_INITIAL_APP","WTS_QUERY_AUDIOENUM_DLL","WTS_QUERY_LOGON_SCREEN_SIZE","WTS_QUERY_MF_FORMAT_SUPPORT","termserv.iwtsprotocolconnection_queryproperty","wtsprotocol/IWTSProtocolConnection::QueryProperty"]
old-location: termserv\iwtsprotocolconnection_queryproperty.htm
tech.root: TermServ
ms.assetid: 129b8314-fa84-414d-93c4-f9320650e2de
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],QueryProperty method, IWTSProtocolConnection.QueryProperty, IWTSProtocolConnection::QueryProperty, PROPERTY_DYNAMIC_TIME_ZONE_INFORMATION, QueryProperty, QueryProperty method [Remote Desktop Services], QueryProperty method [Remote Desktop Services],IWTSProtocolConnection interface, WTS_QUERY_ALLOWED_INITIAL_APP, WTS_QUERY_AUDIOENUM_DLL, WTS_QUERY_LOGON_SCREEN_SIZE, WTS_QUERY_MF_FORMAT_SUPPORT, termserv.iwtsprotocolconnection_queryproperty, wtsprotocol/IWTSProtocolConnection::QueryProperty
req.header: wtsprotocol.h
req.include-header: Wtsdefs.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolConnection::QueryProperty
 - wtsprotocol/IWTSProtocolConnection::QueryProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.QueryProperty
---

# IWTSProtocolConnection::QueryProperty


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::QueryProperty</b> 
    is no longer available for use as of Windows Server 2012. Instead, use 
    <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty">IWRdsProtocolConnection::QueryProperty</a>.]

Retrieves the specified property from the protocol. This method can be  used by other Windows 
    modules to request data  from or send data to the protocol.

## -parameters

### -param QueryType [in]

A <b>GUID</b> that specifies the property. This can be one of the following values.



#### WTS_QUERY_ALLOWED_INITIAL_APP (C77D1B30-5BE1-4c6b-A0E1-BD6D2E5C9FCC)

Sent by the Remote Desktop Services service to determine  whether an initial application should be 
         permitted to run.

On input, the Remote Desktop Services service passes three 
         <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a> structures in the 
         <i>pPropertyEntriesIn</i> parameter:

Input structure 1:

<ul>
<li>pPropertyEntriesIn[0].Type = <b>WTS_VALUE_TYPE_STRING</b></li>
<li>pPropertyEntriesIn[0].u.strVal.pstrVal = <i>application name</i></li>
<li>pPropertyEntriesIn[0].u.strVal.size = <i>length of the name string</i></li>
</ul>
Input structure 2:

<ul>
<li>pPropertyEntriesIn[1].Type = <b>WTS_VALUE_TYPE_STRING</b></li>
<li>pPropertyEntriesIn[1].u.strVal.pstrVal = <i>application parameters</i></li>
<li>pPropertyEntriesIn[1].u.strVal.size = <i>length of the parameter string</i></li>
</ul>
Input structure 3:

<ul>
<li>pPropertyEntriesIn[2].Type = <b>WTS_VALUE_TYPE_ULONG</b></li>
<li>pPropertyEntriesIn[2].u.ulVal = <i>reserved</i></li>
</ul>
On output, pass the following three 
         <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a> structures in the 
         <i>pPropertyEntriesOut</i> parameter. If you want to use the application passed in by the 
         Remote Desktop Services service , copy input structures 1 and 2 to output structures 1 and 2.

Output structure 1:

<ul>
<li>pPropertyEntriesOut[0].Type = <b>WTS_VALUE_TYPE_STRING</b></li>
<li>pPropertyEntriesOut[0].u.strVal.pstrVal = <i>command line including the directory</i></li>
<li>pPropertyEntriesOut[0].u.strVal.size = <i>length of command line</i></li>
</ul>
Output structure 2:

<ul>
<li>pPropertyEntriesOut[1].Type = <b>WTS_VALUE_TYPE_STRING</b></li>
<li>pPropertyEntriesOut[1].u.strVal.pstrVal = <i>application parameters</i></li>
<li>pPropertyEntriesOut[1].u.strVal.size = <i>length of the parameter string</i></li>
</ul>
Output structure 3:

<ul>
<li>pPropertyEntriesOut[2].Type = <b>WTS_VALUE_TYPE_ULONG</b></li>
<li>pPropertyEntriesOut[2].u.ulVal = <i>Any value other than zero to run the application, zero to stop</i></li>
</ul>


#### WTS_QUERY_LOGON_SCREEN_SIZE (8b8e0fe7-0804-4a0e-b279-8660b1df0049)

Used by WinLogon to determine the size of the logon screen.

The <i>pPropertyEntriesIn</i> parameter will be 
         <b>NULL</b>.

Set the <i>pPropertyEntriesOut</i> parameter to the following:

<ul>
<li>pPropertyEntriesOut[0].Type = <b>WTS_VALUE_TYPE_ULONG</b></li>
<li>pPropertyEntriesOut[0].u.ulVal = <i>screen size</i></li>
</ul>
If you do not want to use the default screen size, the protocol must return 
         <b>E_NOTIMPL</b>.



#### WTS_QUERY_AUDIOENUM_DLL (9bf4fa97-c883-4c2a-80ab-5a39c9af00db)

Used by the Remote Desktop Services service to query for the name of the remote audio enumerator DLL.

The <i>pPropertyEntriesIn</i> parameter will be 
         <b>NULL</b>.

Set the <i>pPropertyEntriesOut</i> parameter to the following :

<ul>
<li>pPropertyEntriesOut[0].Type = <b>WTS_VALUE_TYPE_STRING</b></li>
<li>pPropertyEntriesOut[0].u.strVal.pstrVal =  <i>DLL name</i></li>
</ul>
You must allocate the memory for <b>pstrVal</b> by using the 
         <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function.



#### WTS_QUERY_MF_FORMAT_SUPPORT (41869ad0-6332-4dc8-95d5-db749e2f1d94)

Used by the Remote Desktop Media Foundation plug-in to determine the sink objects to be used for specific 
         media formats.

On input, the RCM passes the following 
         <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a> structure in the 
         <i>pPropertyEntriesIn</i> parameter:

<ul>
<li>pPropertyEntriesOut[0].Type = <b>WTS_VALUE_TYPE_BINARY</b></li>
<li>pPropertyEntriesOut[0].u.bVal.pbVal = <a href="/windows/desktop/TermServ/tsmf-support-data-in">TSMF_SUPPORT_DATA_IN</a>
</li>
<li>pPropertyEntriesOut[0].u.bVal.size = Size of <a href="/windows/desktop/TermServ/tsmf-support-data-in">TSMF_SUPPORT_DATA_IN</a>
</li>
</ul>
On output, pass the following 
         <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a> structure in the 
         <i>pPropertyEntriesOut</i> parameter.

<ul>
<li>pPropertyEntriesOut[0].Type = <b>WTS_VALUE_TYPE_BINARY</b></li>
<li>pPropertyEntriesOut[0].u.bVal.pbVal = <a href="/windows/desktop/TermServ/tsmf-support-data-out">TSMF_SUPPORT_DATA_OUT</a>
</li>
<li>pPropertyEntriesOut[0].u.bVal.size = Size of <a href="/windows/desktop/TermServ/tsmf-support-data-out">TSMF_SUPPORT_DATA_OUT</a>
</li>
</ul>


#### PROPERTY_DYNAMIC_TIME_ZONE_INFORMATION (cdfd28e-d0b9-4c1f-a5eb-6d1f6c6535b9)

Used to retrieve the dynamic time zone information from a connection.

The <i>pPropertyEntriesIn</i> parameter will be 
         <b>NULL</b>.

On output, pass the following 
         <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the 
         <i>pPropertyEntriesOut</i> parameter:

<ul>
<li>pPropertyEntriesOut[0].Type = <b>WRDS_VALUE_TYPE_BINARY</b></li>
<li>pPropertyEntriesOut[0].u.bVal.pbVal = <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information">WRDS_DYNAMIC_TIME_ZONE_INFORMATION</a> structure</li>
<li>pPropertyEntriesOut[0].u.bVal.size = Size of <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information">WRDS_DYNAMIC_TIME_ZONE_INFORMATION</a> structure</li>
</ul>

### -param ulNumEntriesIn [in]

An integer that contains the number of 
       <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a> structures passed in the 
       <i>pPropertyEntriesIn</i> argument.

### -param ulNumEntriesOut [in]

An integer that contains the number of 
       <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a> structures passed in the 
       <i>pPropertyEntriesOut</i> argument.

### -param pPropertyEntriesIn [in, optional]

One or more <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a> structures 
       that can be used to help find the requested property information.

### -param pPropertyEntriesOut [out, optional]

One or more <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a> structures 
       that contain the requested property information.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>



<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty">IWRdsProtocolConnection::QueryProperty</a>



<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>



<a href="/windows/desktop/TermServ/tsmf-support-data-in">TSMF_SUPPORT_DATA_IN</a>



<a href="/windows/desktop/TermServ/tsmf-support-data-out">TSMF_SUPPORT_DATA_OUT</a>



<a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information">WRDS_DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WTS_PROPERTY_VALUE</a>