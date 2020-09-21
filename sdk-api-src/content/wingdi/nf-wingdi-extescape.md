---
UID: NF:wingdi.ExtEscape
title: ExtEscape function (wingdi.h)
description: The ExtEscape function enables an application to access device capabilities that are not available through GDI.
helpviewer_keywords: ["CHECKJPEGFORMAT","CHECKPNGFORMAT","DRAWPATTERNRECT","ExtEscape","ExtEscape function [Windows GDI]","GETTECHNOLOGY","GET_PS_FEATURESETTING","PASSTHROUGH","POSTSCRIPT_DATA","POSTSCRIPT_IDENTIFY","POSTSCRIPT_INJECTION","POSTSCRIPT_PASSTHROUGH","QUERYESCSUPPORT","SPCLPASSTHROUGH2","_win32_ExtEscape","gdi.extescape","wingdi/ExtEscape"]
old-location: gdi\extescape.htm
tech.root: xps
ms.assetid: 5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f
ms.date: 12/05/2018
ms.keywords: CHECKJPEGFORMAT, CHECKPNGFORMAT, DRAWPATTERNRECT, ExtEscape, ExtEscape function [Windows GDI], GETTECHNOLOGY, GET_PS_FEATURESETTING, PASSTHROUGH, POSTSCRIPT_DATA, POSTSCRIPT_IDENTIFY, POSTSCRIPT_INJECTION, POSTSCRIPT_PASSTHROUGH, QUERYESCSUPPORT, SPCLPASSTHROUGH2, _win32_ExtEscape, gdi.extescape, wingdi/ExtEscape
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ExtEscape
 - wingdi/ExtEscape
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-RTCore-GDI-DevCaps-l1-1-1.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
api_name:
 - ExtEscape
---

# ExtEscape function


## -description

The <b>ExtEscape</b> function enables an application to access device capabilities that are not available through GDI.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param iEscape [in]

The escape function to be performed. It can be one of the following or it can be an application-defined escape function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CHECKJPEGFORMAT"></a><a id="checkjpegformat"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd183421(v=vs.85)">CHECKJPEGFORMAT</a></b></dt>
</dl>
</td>
<td width="60%">
Checks whether the printer supports a JPEG image.

</td>
</tr>
<tr>
<td width="40%"><a id="CHECKPNGFORMAT"></a><a id="checkpngformat"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd183424(v=vs.85)">CHECKPNGFORMAT</a></b></dt>
</dl>
</td>
<td width="60%">
Checks whether the printer supports a PNG image.

</td>
</tr>
<tr>
<td width="40%"><a id="DRAWPATTERNRECT"></a><a id="drawpatternrect"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd162495(v=vs.85)">DRAWPATTERNRECT</a></b></dt>
</dl>
</td>
<td width="60%">
Draws a white, gray-scale, or black rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="GET_PS_FEATURESETTING"></a><a id="get_ps_featuresetting"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)">GET_PS_FEATURESETTING</a></b></dt>
</dl>
</td>
<td width="60%">
Gets information on a specified feature setting for a PostScript driver.

</td>
</tr>
<tr>
<td width="40%"><a id="GETTECHNOLOGY"></a><a id="gettechnology"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)">GETTECHNOLOGY</a></b></dt>
</dl>
</td>
<td width="60%">
Reports on whether or not the driver is a Postscript driver.

</td>
</tr>
<tr>
<td width="40%"><a id="PASSTHROUGH"></a><a id="passthrough"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd162776(v=vs.85)">PASSTHROUGH</a></b></dt>
</dl>
</td>
<td width="60%">
Allows the application to send data directly to a printer. Supported in compatibility mode and GDI-centric mode.

</td>
</tr>
<tr>
<td width="40%"><a id="POSTSCRIPT_DATA"></a><a id="postscript_data"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd162828(v=vs.85)">POSTSCRIPT_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
Allows the application to send data directly to a printer. Supported only in compatibility mode.

</td>
</tr>
<tr>
<td width="40%"><a id="POSTSCRIPT_IDENTIFY"></a><a id="postscript_identify"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a></b></dt>
</dl>
</td>
<td width="60%">
Sets a PostScript driver to GDI-centric or PostScript-centric mode.

</td>
</tr>
<tr>
<td width="40%"><a id="POSTSCRIPT_INJECTION"></a><a id="postscript_injection"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)">POSTSCRIPT_INJECTION</a></b></dt>
</dl>
</td>
<td width="60%">
Inserts a block of raw data in a PostScript job stream.

</td>
</tr>
<tr>
<td width="40%"><a id="POSTSCRIPT_PASSTHROUGH"></a><a id="postscript_passthrough"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd162831(v=vs.85)">POSTSCRIPT_PASSTHROUGH</a></b></dt>
</dl>
</td>
<td width="60%">
Sends data directly to a PostScript printer driver. Supported in compatibility mode and PostScript-centric mode.

</td>
</tr>
<tr>
<td width="40%"><a id="QUERYESCSUPPORT"></a><a id="queryescsupport"></a><dl>
<dt><b>QUERYESCSUPPORT</b></dt>
</dl>
</td>
<td width="60%">
Determines whether a particular escape is implemented by the device driver.

</td>
</tr>
<tr>
<td width="40%"><a id="SPCLPASSTHROUGH2"></a><a id="spclpassthrough2"></a><dl>
<dt><b><a href="/previous-versions/windows/desktop/legacy/dd145110(v=vs.85)">SPCLPASSTHROUGH2</a></b></dt>
</dl>
</td>
<td width="60%">
Enables applications to include private procedures and other resources at the document level-save context.

</td>
</tr>
</table>

### -param cjInput [in]

The number of bytes of data pointed to by the <i>lpszInData</i> parameter.

### -param lpInData [in]

A pointer to the input structure required for the specified escape. See also Remarks.

### -param cjOutput [in]

The number of bytes of data pointed to by the <i>lpszOutData</i> parameter.

### -param lpOutData [out]

A pointer to the structure that receives output from this escape. This parameter must not be <b>NULL</b> if <b>ExtEscape</b> is called as a query function. If no data is to be returned in this structure, set <i>cbOutput</i> to 0. See also Remarks.

## -returns

The return value specifies the outcome of the function. It is greater than zero if the function is successful, except for the QUERYESCSUPPORT printer escape, which checks for implementation only. The return value is zero if the escape is not implemented. A return value less than zero indicates an error.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Use this function to pass a driver-defined escape value to a device.

Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-escape">Escape</a> function to pass one of the system-defined escape values to a device, unless the escape is one of the defined escapes in <i>nEscape</i>. <b>ExtEscape</b> might not work properly with the system-defined escapes. In particular, escapes in which <i>lpszInData</i> is a pointer to a structure that contains a member that is a pointer will fail.

Note, that the behavior described in this article is the expected behavior, but it is up to the driver to comply with this model.

The variables referenced by <i>lpszInData</i> and <i>lpszOutData</i> should not be the same or overlap. If the input and the output buffer size variables overlap, they may not contain the correct values after the call returns. For the best results, <i>lpszInData</i> and <i>lpszOutData</i> should refer to different variables.

The <a href="/previous-versions/windows/desktop/legacy/dd183421(v=vs.85)">CHECKJPEGFORMAT</a> printer escape function determines whether a printer supports printing a JPEG image.

Before using the <a href="/previous-versions/windows/desktop/legacy/dd183421(v=vs.85)">CHECKJPEGFORMAT</a> printer escape function, call the <a href="/previous-versions/windows/desktop/legacy/ff686811(v=vs.85)">QUERYESCSUPPORT</a> printer escape function to determine whether the driver supports <b>CHECKJPEGFORMAT</b>. For sample code that demonstrates the use of <b>CHECKJPEGFORMAT</b>, see <a href="/windows/desktop/gdi/testing-a-printer-for-jpeg-or-png-support">Testing a Printer for JPEG or PNG Support</a>.

The <a href="/previous-versions/windows/desktop/legacy/dd183424(v=vs.85)">CHECKPNGFORMAT</a> printer escape function determines whether a printer supports printing a PNG image.

Before using the <a href="/previous-versions/windows/desktop/legacy/dd183421(v=vs.85)">CHECKJPEGFORMAT</a> printer escape function, call the <a href="/previous-versions/windows/desktop/legacy/ff686811(v=vs.85)">QUERYESCSUPPORT</a> printer escape function to determine whether the driver supports <b>CHECKJPEGFORMAT</b>. For sample code, see <a href="/windows/desktop/gdi/testing-a-printer-for-jpeg-or-png-support">Testing a Printer for JPEG or PNG Support</a>.

The <a href="/previous-versions/windows/desktop/legacy/dd162495(v=vs.85)">DRAWPATTERNRECT</a> printer escape creates a white, gray scale, or solid black rectangle by using the pattern and rule capabilities of Page Control Language (PCL) on Hewlett-Packard LaserJet or LaserJet-compatible printers. A gray scale is a gray pattern that contains a specific mixture of black and white pixels.

An application should use the <a href="/previous-versions/windows/desktop/legacy/ff686811(v=vs.85)">QUERYESCSUPPORT</a> escape to determine whether the printer is capable of drawing patterns and rules before using the <a href="/previous-versions/windows/desktop/legacy/dd162495(v=vs.85)">DRAWPATTERNRECT</a> escape.


<ul>
<li>Rules drawn with <a href="/previous-versions/windows/desktop/legacy/dd162495(v=vs.85)">DRAWPATTERNRECT</a> are not subject to clipping regions in the device context.</li>
<li>Applications should not try to erase patterns and rules created with <a href="/previous-versions/windows/desktop/legacy/dd162495(v=vs.85)">DRAWPATTERNRECT</a> by placing opaque objects over them. </li>
</ul>


If the printer supports white rules, these can be used to erase patterns created by <a href="/previous-versions/windows/desktop/legacy/dd162495(v=vs.85)">DRAWPATTERNRECT</a>. If the printer does not support white rules, there is no method for erasing these patterns.

If an application cannot use the <a href="/previous-versions/windows/desktop/legacy/dd162495(v=vs.85)">DRAWPATTERNRECT</a> escape and the device is a printer, it should generally use the <a href="/windows/desktop/api/wingdi/nf-wingdi-patblt">PatBlt</a> function instead. Note that if <b>PatBlt</b> is used to print a black rectangle, the application should use the BLACKNESS raster operator. If the device is a plotter, however, the application should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rectangle">Rectangle</a> function.

The <a href="/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)">GET_PS_FEATURESETTING</a> printer escape function retrieves information about a specified feature setting for a PostScript driver.

This escape function is supported only if the PostScript driver is in PostScript-centric mode or in GDI-centric mode. To set the PostScript driver mode, call the <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> escape function.

To perform this operation, call the <b>ExtEscape</b> function with the following parameters.

The <a href="/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)">GET_PS_FEATURESETTING</a> printer escape function is valid if called any time after calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a> function and before calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> function.

The <a href="/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)">GETTECHNOLOGY</a> printer escape function identifies the type of printer driver.

For non-XPSDrv printers, this escape reports whether the driver is a Postscript driver.

For XPSDrv printers, this escape reports whether the driver is the <a href="/windows/desktop/printdocs/microsoft-xps-document-converter--mxdc-">Microsoft XPS Document Converter (MXDC)</a>. If it is, the escape returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06"

The <a href="/previous-versions/windows/desktop/legacy/dd162776(v=vs.85)">PASSTHROUGH</a> printer escape function sends data directly to a printer driver. To perform this operation, call the <b>ExtEscape</b> function with the following parameters.

The <b>PASSTHROUGH</b> printer escape function is supported by PostScript drivers in GDI-centric mode or compatibility mode, but not in PostScript-centric mode. Drivers in PostScript-centric mode can use the <a href="/previous-versions/windows/desktop/legacy/dd162831(v=vs.85)">POSTSCRIPT_PASSTHROUGH</a> escape function. To set a PostScript driver mode, call the <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> escape function.

For PASSTHROUGH data sent by EPSPRINTING or PostScript-centric applications, the PostScript driver will not make any modifications. For PASSTHROUGH data sent by other applications, if the PostScript driver is using BCP (Binary Communication Protocol) or TBCP (Tagged Binary Communication Protocol) output protocol, the driver does the appropriate BCP or TBCP quoting on special characters, as described in "Adobe Serial and Parallel Communications Protocols Specification." This means that the application should send either ASCII or pure binary PASSTHROUGH data.

The <a href="/previous-versions/windows/desktop/legacy/dd162828(v=vs.85)">POSTSCRIPT_DATA</a> printer escape function sends data directly to a printer driver. To perform this operation, call the <b>ExtEscape</b> function with the following parameters.

The <a href="/previous-versions/windows/desktop/legacy/dd162828(v=vs.85)">POSTSCRIPT_DATA</a> function is identical to the <a href="/previous-versions/windows/desktop/legacy/dd162776(v=vs.85)">PASSTHROUGH</a> escape function except that it is supported by PostScript drivers in compatibility mode only. It is not supported by PostScript drivers in PostScript-centric mode or in GDI-centric mode.

Drivers in PostScript-centric mode can use the <a href="/previous-versions/windows/desktop/legacy/dd162831(v=vs.85)">POSTSCRIPT_PASSTHROUGH</a> escape function, and drivers in GDI-centric mode can use the <a href="/previous-versions/windows/desktop/legacy/dd162776(v=vs.85)">PASSTHROUGH</a> escape function. To set a PostScript driver's mode, call the <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> escape function.

The <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> printer escape function sets a PostScript driver to GDI-centric mode or PostScript-centric mode.

To put the driver in GDI-centric or PostScript-centric modes, first call the <a href="/previous-versions/windows/desktop/legacy/ff686811(v=vs.85)">QUERYESCSUPPORT</a> printer escape function to determine whether the driver supports the <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> printer escape function. If so, you can assume the driver is PSCRIPT 5.0. Then, before you call any other printer escape function, you must call <b>POSTSCRIPT_IDENTIFY</b> and specify either <b>PSIDENT_GDICENTRIC</b> or <b>PSIDENT_PSCENTRIC</b>. You must call the <b>QUERYESCSUPPORT</b> and <b>POSTSCRIPT_IDENTIFY</b> printer escape functions before calling any other printer escape function.

<div class="alert"><b>Note</b>  After the PostScript driver is set to GDI-centric mode or PostScript-centric mode, you will not be allowed to call the <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> printer escape function anymore.</div>
<div> </div>
If you do not use the <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> printer escape function, the PostScript driver is in compatibility mode and provides identical support for the <a href="/previous-versions/windows/desktop/legacy/dd162776(v=vs.85)">PASSTHROUGH</a>, <a href="/previous-versions/windows/desktop/legacy/dd162831(v=vs.85)">POSTSCRIPT_PASSTHROUGH</a>, and <a href="/previous-versions/windows/desktop/legacy/dd162828(v=vs.85)">POSTSCRIPT_DATA</a> printer escape functions.

For PostScript drivers that support the <a href="/previous-versions/windows/desktop/legacy/dd162831(v=vs.85)">POSTSCRIPT_PASSTHROUGH</a>, <a href="/previous-versions/windows/desktop/legacy/dd162776(v=vs.85)">PASSTHROUGH</a>, and <b>POSTSCRIPT_PASSTHROUGH</b> printer escape functions are identical.

In PostScript-centric mode, the application is responsible for all PostScript output that marks the paper using the <a href="/previous-versions/windows/desktop/legacy/dd162831(v=vs.85)">POSTSCRIPT_PASSTHROUGH</a> escape function. GDI functions are not allowed. The driver is responsible for the overall document structure and printer control settings. The application can use the <a href="/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)">POSTSCRIPT_INJECTION</a> printer escape function to inject a block of raw data (including DSC comments) into the job stream at specific places.

The <a href="/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)">POSTSCRIPT_INJECTION</a> printer escape function inserts a block of raw data at a specified point in a PostScript job stream.

A PostScript driver supports this escape function in GDI-centric mode or PostScript-centric mode support, but not  in compatibility mode.

To set the PostScript driver's mode, call the <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> escape function.

To perform this operation, call the <b>ExtEscape</b> function with the following parameters.

The driver internally caches the injection data and emits it at appropriate points in the output. The cached information is flushed when it is no longer needed. At the latest, it is flushed after the <a href="/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a> call.

In GDI-centric mode, the application can only inject valid DSC block data by using the <a href="/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)">POSTSCRIPT_INJECTION</a> printer escape function. A valid DSC block must satisfy all of the following conditions:

<ul>
<li>It consists of an integral sequence of "lines."</li>
<li>Each "line" must begin with "%%".</li>
<li>Each "line" except the last line must end with &lt;CR&gt;, &lt;LF&gt;, or &lt;CR&gt;&lt;LF&gt; except for the last line. If the last line does not end with &lt;CR&gt;, &lt;LF&gt;, or &lt;CR&gt;&lt;LF&gt;, the driver appends &lt;CR&gt;&lt;LF&gt; after the last byte of the injection data.</li>
<li>Each "line" must be 255 bytes or less including the "%%" but not counting the &lt;CR&gt;/&lt;LF&gt; line termination.</li>
</ul>
The <a href="/previous-versions/windows/desktop/legacy/dd162831(v=vs.85)">POSTSCRIPT_PASSTHROUGH</a> printer escape function sends data directly to a PostScript printer driver.

A PostScript driver supports this escape function when in PostScript-centric mode or in compatibility mode, but not in GDI-centric mode.

To set the PostScript driver's mode, call the <a href="/previous-versions/windows/desktop/legacy/dd162829(v=vs.85)">POSTSCRIPT_IDENTIFY</a> escape function.

The <a href="/previous-versions/windows/desktop/legacy/ff686811(v=vs.85)">QUERYESCSUPPORT</a> printer escape function checks the implementation of a printer escape function.

The <a href="/previous-versions/windows/desktop/legacy/dd145110(v=vs.85)">SPCLPASSTHROUGH2</a> printer escape function allows applications that print to PostScript devices using EPSPRINTING to include private PostScript procedures and other resources at the document-level save context.

This escape is supported only for backward compatibility with Adobe Acrobat. Other applications should not use this obsolete escape.

The application must call this escape before calling <a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a> so that the driver will cache the data for insertion at the correct point in the PostScript stream. If this escape is supported, the driver will also allow escape <b>DOWNLOADFACE</b> calls prior to <b>StartDoc</b>. The driver internally caches the data to be inserted and the data required by any escape <b>DOWNLOADFACE</b> calls prior to <b>StartDoc</b> and emits them all immediately before %%EndProlog. The sequence of <a href="/previous-versions/windows/desktop/legacy/dd145110(v=vs.85)">SPCLPASSTHROUGH2</a> and <b>DOWNLOADFACE</b> calls will be preserved in the order their data is passed in, that is, a later call results in data output after an earlier call's data. The driver will consider fonts downloaded by pre-<b>StartDoc</b> escape <b>DOWNLOADFACE</b> calls as unavailable for removal during the scope of the job.

This escape is not recorded in EMF files by the operating system, therefore applications must ensure that EMF recording is turned off for those jobs using the escape.


#### Examples

For an example, see <a href="/windows/desktop/gdi/sizing-a-jpeg-or-png-image">Sizing a JPEG or PNG Image</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-escape">Escape</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>