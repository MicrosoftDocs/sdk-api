---
UID: NF:wtsprotocol.IWRdsProtocolConnection.QueryProperty
title: IWRdsProtocolConnection::QueryProperty (wtsprotocol.h)
description: Retrieves a property value from the protocol.
helpviewer_keywords: ["IWRdsProtocolConnection interface [Remote Desktop Services]","QueryProperty method","IWRdsProtocolConnection.QueryProperty","IWRdsProtocolConnection::QueryProperty","PROPERTY_DYNAMIC_TIME_ZONE_INFORMATION","QueryProperty","QueryProperty method [Remote Desktop Services]","QueryProperty method [Remote Desktop Services]","IWRdsProtocolConnection interface","WRDS_QUERY_ALLOWED_INITIAL_APP","WRDS_QUERY_AUDIOENUM_DLL","WRDS_QUERY_LOGON_SCREEN_SIZE","WRDS_QUERY_MF_FORMAT_SUPPORT","termserv.iwrdsprotocolconnection_queryproperty","wtsprotocol/IWRdsProtocolConnection::QueryProperty"]
old-location: termserv\iwrdsprotocolconnection_queryproperty.htm
tech.root: TermServ
ms.assetid: d504a40f-5dc5-4c1b-960f-d41cccef9154
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],QueryProperty method, IWRdsProtocolConnection.QueryProperty, IWRdsProtocolConnection::QueryProperty, PROPERTY_DYNAMIC_TIME_ZONE_INFORMATION, QueryProperty, QueryProperty method [Remote Desktop Services], QueryProperty method [Remote Desktop Services],IWRdsProtocolConnection interface, WRDS_QUERY_ALLOWED_INITIAL_APP, WRDS_QUERY_AUDIOENUM_DLL, WRDS_QUERY_LOGON_SCREEN_SIZE, WRDS_QUERY_MF_FORMAT_SUPPORT, termserv.iwrdsprotocolconnection_queryproperty, wtsprotocol/IWRdsProtocolConnection::QueryProperty
req.header: wtsprotocol.h
req.include-header: Wtsdefs.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - IWRdsProtocolConnection::QueryProperty
 - wtsprotocol/IWRdsProtocolConnection::QueryProperty
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
 - IWRdsProtocolConnection.QueryProperty
---

# IWRdsProtocolConnection::QueryProperty


## -description

Retrieves a property value from the protocol. This method can be used by other Windows modules to request data from or send data to the protocol.

## -parameters

### -param QueryType [in]

A <b>GUID</b> that specifies the requested property. This can be one of the following values.



#### WRDS_QUERY_ALLOWED_INITIAL_APP (C77D1B30-5BE1-4c6b-A0E1-BD6D2E5C9FCC)

Sent by the Remote Desktop Services service to determine  whether an initial application should be permitted to run.

On input, the Remote Desktop Services service passes three <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structures in the <i>pPropertyEntriesIn</i> parameter:

Input structure 1:

<ul>
<li><code>pPropertyEntriesIn[0].Type = </code><b>WRDS_VALUE_TYPE_STRING</b></li>
<li><code>pPropertyEntriesIn[0].u.strVal.pstrVal = </code><i>application name</i></li>
<li><code>pPropertyEntriesIn[0].u.strVal.size = </code><i>length of the name string</i></li>
</ul>
Input structure 2:

<ul>
<li><code>pPropertyEntriesIn[1].Type = </code><b>WRDS_VALUE_TYPE_STRING</b></li>
<li><code>pPropertyEntriesIn[1].u.strVal.pstrVal = </code><i>application parameters</i></li>
<li><code>pPropertyEntriesIn[1].u.strVal.size = </code><i>length of the parameter string</i></li>
</ul>
Input structure 3:

<ul>
<li><code>pPropertyEntriesIn[2].Type = </code><b>WRDS_VALUE_TYPE_ULONG</b></li>
<li><code>pPropertyEntriesIn[2].u.ulVal = </code><i>Reserved</i></li>
</ul>
On output, pass the following three <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structures in the <i>pPropertyEntriesOut</i> parameter. If you want to use the application passed in by the Remote Desktop Services service , copy input structures 1 and 2 to output structures 1 and 2.

Output structure 1:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_STRING</b></li>
<li><code>pPropertyEntriesOut[0].u.strVal.pstrVal = </code><i>command line including the directory</i></li>
<li><code>pPropertyEntriesOut[0].u.strVal.size = </code><i>length of command line</i></li>
</ul>
Output structure 2:

<ul>
<li><code>pPropertyEntriesOut[1].Type = </code><b>WRDS_VALUE_TYPE_STRING</b></li>
<li><code>pPropertyEntriesOut[1].u.strVal.pstrVal = </code><i>application parameters</i></li>
<li><code>pPropertyEntriesOut[1].u.strVal.size = </code><i>length of the parameter string</i></li>
</ul>
Output structure 3:

<ul>
<li><code>pPropertyEntriesOut[2].Type = </code><b>WRDS_VALUE_TYPE_ULONG</b></li>
<li><code>pPropertyEntriesOut[2].u.ulVal = </code><i>Any value other than zero to run the application, zero to stop</i></li>
</ul>


#### WRDS_QUERY_LOGON_SCREEN_SIZE (8b8e0fe7-0804-4a0e-b279-8660b1df0049)

Used by WinLogon to determine the size of the logon screen.

The <i>pPropertyEntriesIn</i> parameter will be <b>NULL</b>.

Set the <i>pPropertyEntriesOut</i> parameter to the following:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_ULONG</b></li>
<li><code>pPropertyEntriesOut[0].u.ulVal = </code><i>screen size</i></li>
</ul>
If you do not want to use the default screen size, the protocol must return <b>E_NOTIMPL</b>.



#### WRDS_QUERY_AUDIOENUM_DLL (9bf4fa97-c883-4c2a-80ab-5a39c9af00db)

Used by the Remote Desktop Services service to query for the name of the remote audio enumerator DLL.

The <i>pPropertyEntriesIn</i> parameter will be <b>NULL</b>.

Set the <i>pPropertyEntriesOut</i> parameter to the following:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_STRING</b></li>
<li><code>pPropertyEntriesOut[0].u.strVal.pstrVal =  </code><i>DLL name</i></li>
</ul>
You must allocate the memory for <b>pstrVal</b> by using the <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function.



#### WRDS_QUERY_MF_FORMAT_SUPPORT (41869ad0-6332-4dc8-95d5-db749e2f1d94)

Used by the Remote Desktop Media Foundation plug-in to determine the sink objects to be used for specific media formats.

On input, the RCM passes the following  <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the <i>pPropertyEntriesIn</i> parameter:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_BINARY</b></li>
<li><code>pPropertyEntriesOut[0].u.bVal.pbVal = </code><a href="/windows/desktop/TermServ/tsmf-support-data-in">TSMF_SUPPORT_DATA_IN</a> structure</li>
<li><code>pPropertyEntriesOut[0].u.bVal.size = </code>size of <a href="/windows/desktop/TermServ/tsmf-support-data-in">TSMF_SUPPORT_DATA_IN</a> structure</li>
</ul>
On output, pass the following <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the <i>pPropertyEntriesOut</i> parameter:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_BINARY</b></li>
<li><code>pPropertyEntriesOut[0].u.bVal.pbVal = </code><a href="/windows/desktop/TermServ/tsmf-support-data-out">TSMF_SUPPORT_DATA_OUT</a> structure</li>
<li><code>pPropertyEntriesOut[0].u.bVal.size = </code>Size of <a href="/windows/desktop/TermServ/tsmf-support-data-out">TSMF_SUPPORT_DATA_OUT</a> structure</li>
</ul>


#### PROPERTY_DYNAMIC_TIME_ZONE_INFORMATION (cdfd28e-d0b9-4c1f-a5eb-6d1f6c6535b9)

Used to retrieve the dynamic time zone information from a connection.

The <i>pPropertyEntriesIn</i> parameter will be <b>NULL</b>.

On output, pass the following <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the <i>pPropertyEntriesOut</i> parameter:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_BINARY</b></li>
<li><code>pPropertyEntriesOut[0].u.bVal.pbVal = </code><a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information">WRDS_DYNAMIC_TIME_ZONE_INFORMATION</a> structure</li>
<li><code>pPropertyEntriesOut[0].u.bVal.size = </code>Size of <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information">WRDS_DYNAMIC_TIME_ZONE_INFORMATION</a> structure</li>
</ul>


#### CONNECTION_PROPERTY_CURSOR_BLINK_DISABLED (4b150580-fea4-4d3c-9de4-7433a66618f7)

Used to determine whether cursor blink should be disabled.

The <i>pPropertyEntriesIn</i> parameter will be <b>NULL</b>.

On output, pass the following <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the <i>pPropertyEntriesOut</i> parameter:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_ULONG</b></li>
<li><code>pPropertyEntriesOut[0].u.ulVal = </code><i>1 to disable cursor blink, 0 otherwise</i></li>
</ul>

#### PROPERTY_TYPE_GET_FAST_RECONNECT (6212d757-0043-4862-99c3-9f3059ac2a3b)

Used by the Remote Desktop Services service to determine the mode of reconnection to be used.

The <i>pPropertyEntriesIn</i> parameter will be <b>NULL</b>.

On output, pass the following <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the <i>pPropertyEntriesOut</i> parameter:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_ULONG</b></li>
<li><code>pPropertyEntriesOut[0].u.ulVal = </code><i>0 to disable fast reconnect, 1 for Basic Fast Reconnect, 2 for Enhanced Fast Reconnect</i></li>
</ul>

#### PROPERTY_TYPE_GET_FAST_RECONNECT_USER_SID (197c427a-0135-4b6d-9c5e-e6579a0ab625)

Used by the Remote Desktop Services service during Enhanced Fast Reconnect to retrieve the User SID by which sessions to be reconnected to are filtered.

The <i>pPropertyEntriesIn</i> parameter will be <b>NULL</b>.

On output, pass the following <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the <i>pPropertyEntriesOut</i> parameter:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_STRING</b></li>
<li><code>pPropertyEntriesIn[0].u.strVal.pstrVal = </code><i>User SID to be used as session filter</i></li>
<li><code>pPropertyEntriesIn[0].u.strVal.size = </code><i>Length of User SID including the null terminating character</i></li>
</ul>
You must allocate the memory for <b>pstrVal</b> by using the <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function.

#### PROPERTY_TYPE_ENABLE_UNIVERSAL_APPS_FOR_CUSTOM_SHELL (ed2c3fda-338d-4d3f-81a3-e767310d908e)

Used by the Remote Desktop Services service determine if ShellAppRuntime.exe will be launched before any Custom Shells during session creation. ShellAppRuntime.exe implements Universal App support for Custom Shells. This is not enabled by default (equivalent to passing zero). This is available in Windows versions that are Server 2019 and above or Windows 10 multi-session Build 18950 and above.

The <i>pPropertyEntriesIn</i> parameter will be <b>NULL</b>.

On output, pass the following <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the <i>pPropertyEntriesOut</i> parameter:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_ULONG</b></li>
<li><code>pPropertyEntriesOut[0].u.ulVal = </code><i>0 to not enable Universal Apps Support for Custom Shells, 1 Enable Universal Apps Support for Custom Shells</i></li>
</ul>

#### CONNECTION_PROPERTY_IDLE_TIME_WARNING (693f7ff5-0c4e-4d17-b8e0-1f70325e5d58)

Used to determine whether a logoff warning prompt is displayed when the idle timer expires.

The <i>pPropertyEntriesIn</i> parameter will be <b>NULL</b>.

On output, pass the following <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structure in the <i>pPropertyEntriesOut</i> parameter:

<ul>
<li><code>pPropertyEntriesOut[0].Type = </code><b>WRDS_VALUE_TYPE_ULONG</b></li>
<li><code>pPropertyEntriesOut[0].u.ulVal = </code><i>0 to disable warning prompt, 1 to enable it</i></li>
</ul>

### -param ulNumEntriesIn [in]

The number of entries in the <i>pPropertyEntriesIn</i> array.

### -param ulNumEntriesOut [in]

The number of entries in the <i>pPropertyEntriesOut</i> array.

### -param pPropertyEntriesIn [in, optional]

An array of pointers to <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structures that can be used to help find the requested property information.

### -param pPropertyEntriesOut [out, optional]

An array of pointers to <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_property_value">WRDS_PROPERTY_VALUE</a> structures that receive the requested property values.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>
